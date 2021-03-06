onBeforeDrop
=============

@short:
	fires before a dragged item is released over the droppable area

@params:
- context		object				drag-n-drop context object 
- ev 			Event object		a native event object

@returns:

- result		boolean			returning false will prevent further drag-and-drop processing

@example:
$$("fmanager").attachEvent("onBeforeDrop",function(context,ev){
    // your code
    return true;
});

@template:	api_event
@descr:

The properties of the context object are:

- from - (object) the source object
- to - (object) the target object
- source - (array) the ID of the dragged item(s)
- target - (string) the ID of the drop target, null for drop on empty space
- start - (string) the ID from which DnD started

@relatedsample:
64_file_manager/02_events/03_drag.html