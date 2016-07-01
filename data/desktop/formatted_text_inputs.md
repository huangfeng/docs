Formatted Text Inputs
=======================

You can specify the [pattern](api/ui.text_pattern_config.md) of a text input formatting. A pattern presents an object with two properties:

- mask - a string that consists of the "#" signs for input characters (can be restricted by the *allow* parameter) and pattern symbols, such as hyphens, dots, spaces, etc.
- allow - a set of characters that are allowed for entering into the field regardless of their position

~~~js
{ 
	view:"text", 
  	name:"phone", 
    label:"Phone", 
    pattern:{ mask:"###-## ########", allow:/[0-9]/g}
}
~~~

A pattern can also be set as a string. In this case the *allow* property will take the default value (/[A-Za-z0-9]/g).  

~~~js
{ view:"text", name:"phone", label:"Phone", pattern:"###-## ########"}
~~~

##Preset Patterns


There are three predefined patterns for text formatting that are described in the **webix.patterns** collection:

- phone - defines the format of entering a phone number
- card - sets the format of entering a credit card number
- date - specifies the format of entering a date

The predefined patterns are stored as "property-value" pairs, where *property* is the rule name and *value* is an object with *mask* and *allow* properties.

~~~js
webix.patterns = {
	phone:{ mask:"+# (###) ###-####", 	allow:/[0-9]/g },
	card: { mask:"#### #### #### ####", allow:/[0-9]/g },
	date: { mask:"####-##-## ##:##", 	allow:/[0-9]/g }
};
~~~


You can redefine a preset pattern or create a new one through the *webix.patterns* class:

~~~js
// redefine a preset "phone" pattern
webix.patterns.phone = {
	mask:"#### ### #####", allow:/[0-9]/g 
};

// create a new "custom" pattern
webix.patterns.custom = {
	mask:"## ## - ### #####", allow:/[0-9]/g 
};

//or
webix.patterns.custom = "## ## - ### #####";
~~~


##Getting Input Values

You can get the value of an input. There are two variants to do that depending on the input type: 

- using the api/link/ui.text_getvalue.md for usual inputs

~~~js
$$("text1").getValue(); // returns "1234567"
~~~

- using the *getText()* method to get value from a text input that has a formatting pattern set in its node:

~~~js
$$("text1").getText(); // returns "12-345 67"
~~~

{{sample 60_pro/02_form/09_formatted_input.html}}


##Validating Formatted Text Inputs 

When a text input with a pattern is initialized, a rule for its formatting is generated automatically. 
It is applied during validation and checks whether the length of the formatted value complies with the mask and whether it contains only allowed characters. 

However, you can set another [validation rule](desktop/data_validation.md#validationrules) for such input using the *validate* property.
Then the specified validation rule will be applied instead of the generated one.

You can also specify a validation message for a text input using the api/link/ui.textarea_invalidmessage_config.md property. The text of validation message can be
[localized](desktop/formatted_text_inputs.md#localize).

For example, you can specify a rule for validating a Master Card number:

~~~js
var form = webix.ui({
    view:"form", 
    elements:[
      { view:"text", name:"phone",label:"Phone number", pattern:webix.patterns.phone},
      { view:"text", name:"card", label:"Credit card", pattern:webix.patterns.card, 
          validate:function(value){
            return /^5[1-5][0-9]{14}$/.test(value);
      }, invalidMessage:"Invalid card number"}
    ]  
});

form.validate();

form.elements.phone.validate();
form.elements.card.validate();
~~~

The "phone" input is validated according to the autogenerated rule.

The "card" input is validated according to the custom rule, set by a function in the *validate* property.

{{note
Pay attention that inputs should be put into a form, as to validate a separate input you need to address to it via form elements collection. 
}}

<h3 id="localize">Localizing validation message</h3>

To set a text of validation message [for a particular locale](desktop/localization.md#alteringalocale),
you should redefine the text of the *invalidMessage* property and set the same locale to apply the changes:

~~~js
webix.i18n.controls.invalidMessage = "Invalid message text";
webix.i18n.setLocale();
~~~

This message will be applied for all text inputs with patterns, unless they have their own messages specified.

So, in general, validation of inputs with patterns is carried out in the same way as common desktop/data_validation.md. 

{{sample 60_pro/02_form/10_formatted_inputs_validation.html}}