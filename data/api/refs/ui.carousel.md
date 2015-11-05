ui.carousel 
=============


{{memo A container control that provides continuous, circular navigation through a set of pictorial content blocks. One block is visible at a time. }}

The control supports any content inside of it. The content blocks can be arranged vertically or horizontally, supplemented or not with the navigation control panel. Check [carousel](desktop/carousel.md) documentation for more detailed description.

### Constructor

~~~js
	var carousel = webix.ui({
		view:"carousel", 
		container:"mydiv", 
		...config options goes here..
	})
	//or, in case of jQuery
	$("#mydiv").webix_carousel({
		...config options goes here..
	});
~~~
### Where to start

- [Overview of Carousel Widget](desktop/carousel.md)
- [Samples](http://docs.webix.com/samples/26_carousel/index.html)

<div class='webixdoc_parents'><span>Based on: </span>
<a href="api/refs/eventsystem.md">EventSystem</a>, <a href="api/refs/navigationbuttons.md">NavigationButtons</a>, <a href="api/refs/ui.view.md">ui.view</a>, <a href="api/refs/ui.baseview.md">ui.baseview</a>, <a href="api/refs/settings.md">Settings</a>, <a href="api/refs/destruction.md">Destruction</a>, <a href="api/refs/basebind.md">BaseBind</a>, <a href="api/refs/uiextension.md">UIExtension</a></div>


<div class='h2'>Methods</div>

{{api
- api/link/ui.carousel_adjust.md - adjusts the component to the size of the parent HTML container
- api/ui.carousel_adjustscroll.md - adjusts scrolling direction to screen mode (vertical or horizontal)
- api/link/ui.carousel_attachevent.md - attaches the handler to an inner event of the component (allows behaviour customizations)
- api/link/ui.carousel_bind.md - binds components
- api/link/ui.carousel_blockevent.md - temporarily blocks triggering of ALL events of the calling object
- api/link/ui.carousel_callevent.md - calls an inner event
- api/link/ui.carousel_define.md - redefines a single configuration property (or a hash of properties)
- api/link/ui.carousel_destructor.md - destructs the calling object
- api/link/ui.carousel_detachevent.md - detaches a handler from an event (which was attached before by the attachEvent method)
- api/link/ui.carousel_disable.md - disables the calling view (makes it dimmed and unclickable)
- api/link/ui.carousel_enable.md - enables the calling view that was disabled by the 'disable' method
- api/ui.carousel_getactiveid.md - gets the id of the current selected item
- api/ui.carousel_getactiveindex.md - gets the index of the current active item
- api/link/ui.carousel_getchildviews.md - returns child views of the calling component
- api/link/ui.carousel_getformview.md - returns master form for the input
- api/ui.carousel_getlayout.md - gets layout object with carousel views
- api/link/ui.carousel_getnode.md - returns the main HTML container for the calling object
- api/link/ui.carousel_getparentview.md - returns the parent view of the component
- api/link/ui.carousel_gettopparentview.md - returns top parent view
- api/link/ui.carousel_hasevent.md - checks whether the component has the specified event
- api/link/ui.carousel_hide.md - hides the view
- api/link/ui.carousel_isenabled.md - checks whether the view is enabled
- api/link/ui.carousel_isvisible.md - checks whether the view is visible
- api/link/ui.carousel_mapevent.md - routes events from one object to another
- api/link/ui.carousel_resize.md - adjusts the view to a new size
- api/ui.carousel_scrollto.md - scrolls the carousel and scrollview container to a certain position
- api/ui.carousel_setactive.md - selects the item with the specified id
- api/ui.carousel_setactiveindex.md - selects the item with the specified index
- api/link/ui.carousel_show.md - makes the component visible
- api/ui.carousel_shownext.md - shows the next item of the carousel
- api/ui.carousel_showprev.md - shows the previous item of the carousel
- api/link/ui.carousel_unbind.md - breaks "bind" link
- api/link/ui.carousel_unblockevent.md - cancels blocking events that was enabled by the 'blockEvent' command
}}


<div class='h2'>Events</div>


{{api
- api/link/ui.carousel_onafterscroll_event.md - occurs when some webix view has been scrolled
- api/link/ui.carousel_onbindrequest_event.md - fires when the component is ready to receive data from the master component
- api/link/ui.carousel_onblur_event.md - fires when focus is moved out of the view
- api/link/ui.carousel_ondestruct_event.md - occurs when component destroyed
- api/link/ui.carousel_onfocus_event.md - fires when a view gets focus
- api/link/ui.carousel_onkeypress_event.md - occurs when keyboard key is pressed for the control in focus
- api/link/ui.carousel_onlongtouch_event.md - fires on holding finger in some position for a certain period of time
- api/ui.carousel_onshow_event.md - fires when a new view is shown in carousel
- api/link/ui.carousel_onswipex_event.md - occurs on a horizontal swipe movement
- api/link/ui.carousel_onswipey_event.md - occurs on a vertical swipe movement
- api/link/ui.carousel_ontimedkeypress_event.md - fires after typing has been finished in the field
- api/link/ui.carousel_ontouchend_event.md - occurs when the touch event is ended
- api/link/ui.carousel_ontouchmove_event.md - occurs during touch movement
- api/link/ui.carousel_ontouchstart_event.md - when some webix view has been touched
- api/link/ui.carousel_onviewresize_event.md - view size was changed by resizer
}}


<div class='h2'>Properties</div>

{{api
- api/link/ui.carousel_animate_config.md - defines or disables view change animation.
- api/link/ui.carousel_borderless_config.md - used to hide the component borders
- api/ui.carousel_cols_config.md - array of views objects arranged horizontally
- api/link/ui.carousel_container_config.md - an html container (or its id) where the component needs initializing
- api/link/ui.carousel_css_config.md - the name of a css class that will be applied to the view container
- api/link/ui.carousel_disabled_config.md - indicates whether an item is enabled or not
- api/link/ui.carousel_gravity_config.md - sets the view gravity (1 by default)
- api/link/ui.carousel_height_config.md - sets the height of the component
- api/link/ui.carousel_hidden_config.md - defines whether the view will be hidden initially
- api/link/ui.carousel_id_config.md - the component ID
- api/link/ui.carousel_maxheight_config.md - sets the maximum height for the view
- api/link/ui.carousel_maxwidth_config.md - sets the maximum width for the view
- api/link/ui.carousel_minheight_config.md - sets the minimal height for the view
- api/link/ui.carousel_minwidth_config.md - sets the minimal width for the view
- api/link/ui.carousel_navigation_config.md - defines navigation parameters
- api/link/ui.carousel_on_config.md - allows attaching custom handlers to inner events of the component
- api/ui.carousel_rows_config.md - array of views arranged vertically
- api/ui.carousel_scrollspeed_config.md - speed of scrolling ('300ms' by default)
- api/ui.carousel_type_config.md - defines the layout borders
- api/link/ui.carousel_width_config.md - sets the width of the component
}}





<div class='h2'>Other</div>


{{api
- api/link/ui.carousel_$getsize_other.md - returns the current size of the component
- api/link/ui.carousel_$height_other.md - current height of the view
- api/link/ui.carousel_$scope_other.md - scope for resolving event and method names
- api/link/ui.carousel_$setsize_other.md - sets the component size
- api/link/ui.carousel_$skin_other.md - method, which will be called when skin defined
- api/link/ui.carousel_$view_other.md - reference to top html element of the view
- api/link/ui.carousel_$width_other.md - current width of the view
- api/link/ui.carousel_config_other.md - all options from initial component configuration
- api/link/ui.carousel_name_other.md - indicates the name of the component (a read-only property)
}}


@index:
- api/refs/ui.carousel_methods.md
- api/refs/ui.carousel_props.md
- api/refs/ui.carousel_events.md
- api/refs/ui.carousel_others.md

