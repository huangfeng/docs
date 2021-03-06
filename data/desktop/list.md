List
===========

##API Reference

- [Methods, properties and events](api/refs/ui.list.md)
- [Samples](http://docs.webix.com/samples/05_list/index.html)

##Overview

List is a ui-related component that inherits from [view](desktop/view.md) and presents listed data items. The webix library offers three
variations of list apart from the standard one - [grouplist](desktop/grouplist.md), [x-list](desktop/xlist.md) and 
[unitlist](desktop/unitlist.md). <br>


<img style="display:block; margin-left:auto;margin-right:auto;" src="desktop/list.png"/>

##Initialization

~~~js
webix.ui({
	view:"list",
	template:"...",
	data:..//variable || path || dataset
});
~~~

{{sample 05_list/01_list.html }}

You can load data in any of the supported [data formats](desktop/data_types.md). 

##Working with List

- desktop/data_object.md
- [Data Loading](desktop/data_loading.md). 
- [Defining Data Template](desktop/html_templates.md).
- [Adding/Deleting Items](desktop/add_delete.md).
- [Editing Data](desktop/edit.md).
- [Data Filtering and Sorting](desktop/filter_sort.md)
- [Selection](desktop/selection.md)
- [Paging](desktop/paging.md)
- [Adding Active Elements to List Items](desktop/active_content.md)
- desktop/export_png.md
- desktop/data_components_export.md

{{note
Note that there's no built-in possibility to edit data with List. You should create a prototype *editlist* object beforehand.
}}


##Related Articles

- [Setting Dimensions for the Components](desktop/dimensions.md)
- [Dynamic Resizing and Adjustment](desktop/resizing.md)
- [Redefinition of the Components](desktop/redefinition.md)
- [List CSS Image Map](desktop/list_css.md)

@index:
- desktop/xlist.md
