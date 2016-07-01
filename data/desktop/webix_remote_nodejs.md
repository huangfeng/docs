Using Webix Remote with Node.js
==============================

This guide will give you the idea of how you can use Webix Remote for integrating the Webix library with Node.js.

##Installation note

To install Webix Remote, simply run the command below in the command line:

~~~js
npm install webix-remote
~~~


##Server-side code

On the server side you need to include the "webix-remote" dependency. 

Then you should make connection to the server to get access to the server-side API.
Let's put the call of the *server()* function into a variable. We will use it for working with server methods:

~~~js
var remote = require("webix-remote");
var api = remote.server();
~~~

After that you will be able to apply server-side API in your code.
For example, you can use *setMethod()* API that registers new methods to use them later in the client code. 

The setMethod() method takes two parameters:

- name - the function's name
- function -  the function's description 


Let's apply this method to add the *save* function that will save changes in an element by its id. 

~~~js
// adding a "save" function
api.setMethod("save", function(){
	// saving logic
});
~~~

Now you can apply it on the client side.

##Client-side code

On the client side you need to include the path to the server-side API after the *webix.js* file on the page:

~~~html
<script src='webix.js'></script>
<script src='/api'></script>
<script>
   // actions' description
</script>
~~~

After that you can describe operations that should be performed with data and get the result. To address to the server you need to use the **webix.remote** object.

Let's use the *save* function that was added on the server and send a request for saving changes in the element with the id=12. 
We will write the result of the operation into the *result* variable:

~~~js
var result = webix.remote.save("12");
~~~

Webix Remote loads data asynchronously. The client side will get a promise of data first, while real data will come later. 
The *result* in our example is a promise.

The use of promises allows avoiding delays in the page rendering.


##Passing special parameters

You can pass some additional parameters to the functions created on the server. For example, you can use the *$req* parameter 
that will contain request parameters:

~~~js
api.setMethod("add", function(a,b,$req){
    return a+b+$req.session.userBonus;
});
~~~

The client-side code can look like this:

~~~js
webix.remote.add(1,2);
~~~

Besides usual arguments the *add* function on the client will get a request object with parameters about the current user session.


##Setting static data

You can specify some static data on the server which will be available on the client. It can be useful while processing user sessions for storing user data 
and sharing it with the client side, when needed. 

Pay attention that the data generation method will be called just once - during the API initialization.

To specify static data, you need to use the *setData()* method and pass two arguments to it:

- name - (string) the name of parameter that will be set as static
- handler - (function) the function that will take the request object and return the result

For example, on the server side we set the "$user" parameter. The function specified as the second parameter will get a request object and
return the user id:

~~~js
api.setData("$user", function(req){
    return req.user.id;
});
~~~

You can also pass some value instead of the handler as the second parameter :

~~~js
api.setData("$user",1);
~~~

On the client the user data will be available in the following way:

~~~js
var user = webix.remote.$user;
~~~


##API Access Levels

Webix Remote provides the possibility to limit access to API according to the user's access level. It means that the user will be able to use this or that method
depending on his/her predefined role.

To implement such a limitation, you need to specify the role that allows using the method during the method's creation like this:

~~~js
api.setMethod("role@method_name", function(){
   // some code
});
~~~

For example, you can limit access to the "add" method by the "admin" role. 

~~~js
api.setMethod("admin@add", function(a,b){
    return a+b;
});
~~~

The access levels are defined by the access modificator specified with the *req.session* object:

- all methods for which the access modificator isn't set are allowed by default
- if *req.session.user* exists, methods for which the "user" modificator is set are allowed
- if *req.session.user.role* exists, methods for which the modificator of a partucular role is set are allowed

Let's assume that we have the following rule:

~~~js
req.session = { user: { role:"admin,levelB"}}
~~~

In this case the *add* function will be allowed for users with the *"user"*, *"user.role=admin"* and *"user.role=levelB"* access modificators. 
For a user with a different role the method will be unavailable:

~~~js
api.setMethod("user@add1", (a,b) => a+b ); //allowed
api.setMethod("admin@add2", (a,b) => a+b ); //allowed
api.setMethod("levelC@add3", (a,b) => a+b ); //blocked
~~~

###Setting custom logic for access levels

Instead of setting several user verification rules, you can define one access level rule by using the *$access* parameter. For example:

~~~js
api.$access = function(req){
    return { 
        user : !!req.user,
        admin: req.user && req.user.id == 1 
    };
};
~~~

The above code will check whether a user exists and whether he/she possesses the admin role. 