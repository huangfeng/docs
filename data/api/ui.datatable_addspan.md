addSpan
=============

@short: adds colspan or rowspan to the datatable

@edition:pro

@params:
- id				string			id of the row that starts colspan/rowspan
- column			string							id of the column that starts colspan/rowspan
- width				number							how many columns should the span include
- height			number							how many rows should the span include
* value				string 	 						value that the span area should display
* css				string 	 						css class that should be applied to the span area

@example:

grid.addSpan(1, "country", 1, 3);
grid.refresh();

@related:
	datatable/rowspans_colspans.md
@relatedapi:
	api/ui.datatable_spans_config.md
    api/ui.datatable_removespan.md
    api/ui.datatable_getspan.md
@template:	api_method
@edition:  pro
@descr:
To enable the rowspans and colspans functionality, you should set the **spans** parameter with the *true* value in the datatable configuration:

~~~js
webix.ui({
    view:"datatable",
    columns:[...],
    spans:true
    ...
});
~~~


The method can as well take an array of arrays with the same configuration (*id, column, width, height, value, css*) to define several spans at a time.

~~~js
grid.addSpan([
	[1, "country", 1, 3],
    [4, "country", 1, 2],
    [6, "country", 1, 3]
]);
~~~

**Defaults:**

- default values for span **width** and **height** are 1;
- span **value** parameter is optional and used if a custom text for the cell is required. If you  need to display the initial value, omit this field or pass an empty value ("", null);
- span **css** is optional. By default, colspans and rowspans don't feature any special styling. 