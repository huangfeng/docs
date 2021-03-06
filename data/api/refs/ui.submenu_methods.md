Methods
=======

{{api
- api/link/ui.submenu_add.md - adds an item to the store
- api/link/ui.submenu_addcss.md - applied CSS class to a component item
- api/link/ui.submenu_adjust.md - adjusts the component to the size of the parent HTML container
- api/link/ui.submenu_attachevent.md - attaches the handler to an inner event of the component (allows behaviour customizations)
- api/link/ui.submenu_bind.md - binds components
- api/link/ui.submenu_blockevent.md - temporarily blocks triggering of ALL events of the calling object
- api/link/ui.submenu_callevent.md - calls an inner event
- api/link/ui.submenu_clearall.md - removes all items from the component
- api/link/ui.submenu_clearcss.md - removes css class from all items
- api/link/ui.submenu_clearvalidation.md - removes all validation marks from the component
- api/link/ui.submenu_close.md - removes a window
- api/link/ui.submenu_copy.md - copies an item to the same or another object
- api/link/ui.submenu_count.md - returns the number of currently visible items
- api/link/ui.submenu_customize.md - redefines the "type" property
- api/link/ui.submenu_define.md - redefines a single configuration property (or a hash of properties)
- api/link/ui.submenu_destructor.md - destructs the calling object
- api/link/ui.submenu_detachevent.md - detaches a handler from an event (which was attached before by the attachEvent method)
- api/link/ui.submenu_disable.md - disables the calling view (makes it dimmed and unclickable)
- api/link/ui.submenu_disableitem.md - disables menu item
- api/link/ui.submenu_enable.md - enables the calling view that was disabled by the 'disable' method
- api/link/ui.submenu_enableitem.md - enables menu item
- api/link/ui.submenu_exists.md - checks whether an item with the specified id exists
- api/link/ui.submenu_filter.md - filters the component
- api/link/ui.submenu_find.md - returns rows that match the criterion
- api/link/ui.submenu_getbody.md - gets the ui view of the window body
- api/link/ui.submenu_getchildviews.md - returns child views of the calling component
- api/link/ui.submenu_getfirstid.md - returns the ID of the first item
- api/link/ui.submenu_getformview.md - returns master form for the input
- api/link/ui.submenu_gethead.md - gets the ui view of the window header
- api/link/ui.submenu_getidbyindex.md - returns the id of the item with the specified index
- api/link/ui.submenu_getindexbyid.md - returns the index of the item with the specified id
- api/link/ui.submenu_getitem.md - gets the object of the data item with the specified id
- api/link/ui.submenu_getitemnode.md - returns HTML element of the item
- api/link/ui.submenu_getlastid.md - returns the id of the last item
- api/link/ui.submenu_getmenu.md - gets object of a menu/submenu where an item is located
- api/link/ui.submenu_getmenuitem.md - search for menu item in submenus
- api/link/ui.submenu_getnextid.md - returns the ID of an item which is positioned the specified step after the specified item
- api/link/ui.submenu_getnode.md - returns the main HTML container for the calling object
- api/link/ui.submenu_getpage.md - returns the currently visible page in case of paged view
- api/link/ui.submenu_getpager.md - returns the pager object associated with the component
- api/link/ui.submenu_getparentview.md - returns the parent view of the component
- api/link/ui.submenu_getprevid.md - returns the ID of an item which is positioned the specified step before the specified item
- api/link/ui.submenu_getscrollstate.md - returns the scroll position
- api/link/ui.submenu_getselectedid.md - returns the id(s) of the selected item(s)
- api/link/ui.submenu_getselecteditem.md - returns selected object
- api/link/ui.submenu_getsubmenu.md - gets the submenu object of a menu item (if any)
- api/link/ui.submenu_gettopmenu.md - returns top menu object
- api/link/ui.submenu_gettopparentview.md - returns top parent view
- api/link/ui.submenu_getvisiblecount.md - returns the number of items that can be seen with the current view height
- api/link/ui.submenu_hascss.md - checks if item has specific css class
- api/link/ui.submenu_hasevent.md - checks whether the component has the specified event
- api/link/ui.submenu_hide.md - hides the view
- api/link/ui.submenu_hideitem.md - hides menu item
- api/link/ui.submenu_isenabled.md - checks whether the view is enabled
- api/link/ui.submenu_isselected.md - checks whether the specified item is selected or not
- api/link/ui.submenu_isvisible.md - checks whether the view is visible
- api/link/ui.submenu_load.md - loads data from an external data source.
- api/link/ui.submenu_loadnext.md - sends a request to load the specified number of records to the end of the clientside dataset or to the specified position
- api/link/ui.submenu_locate.md - gets the id of an item from the specified HTML event
- api/link/ui.submenu_mapevent.md - routes events from one object to another
- api/link/ui.submenu_move.md - moves the specified item to the new position
- api/link/ui.submenu_movebottom.md - moves the specified item to the last position
- api/link/ui.submenu_movedown.md - increases the item index and moves the item to the new position
- api/link/ui.submenu_moveselection.md - moves selection in the specified direction
- api/link/ui.submenu_movetop.md - moves the specified item to the first position
- api/link/ui.submenu_moveup.md - decreases the item index and moves the item to the new position
- api/link/ui.submenu_parse.md - loads data to the component from an inline data source
- api/link/ui.submenu_refresh.md - repaints the whole view or a certain item
- api/link/ui.submenu_remove.md - removes the specified item/items from datastore
- api/link/ui.submenu_removecss.md - removes CSS class from a component item
- api/link/ui.submenu_render.md - renders the specified item or the whole component
- api/link/ui.submenu_resize.md - adjusts the view to a new size
- api/link/ui.submenu_resizechildren.md - resizes all children of the calling component
- api/link/ui.submenu_scrollto.md - scrolls the data container to a certain position
- api/link/ui.submenu_select.md - selects the specified item(s)
- api/link/ui.submenu_selectall.md - selects all items or the specified range
- api/link/ui.submenu_serialize.md - serializes data to a JSON object
- api/link/ui.submenu_setpage.md - makes the specified page visible (assuming that the pager was defined )
- api/link/ui.submenu_setposition.md - sets window's position
- api/link/ui.submenu_show.md - makes the component visible
- api/link/ui.submenu_showitem.md - scrolls the component to make the specified item visible
- api/link/ui.submenu_sizetocontent.md - adjusts the size of menu and its submenus to their content
- api/link/ui.submenu_sort.md - sorts datastore
- api/link/ui.submenu_sync.md - allows syncing two copies of data (all or just a part of it) from one DataCollection to another
- api/link/ui.submenu_unbind.md - breaks "bind" link
- api/link/ui.submenu_unblockevent.md - cancels blocking events that was enabled by the 'blockEvent' command
- api/link/ui.submenu_unselect.md - removes selection from the specified item
- api/link/ui.submenu_unselectall.md - removes selection from all items
- api/link/ui.submenu_updateitem.md - sets properties of the data item
- api/link/ui.submenu_validate.md - validates one record or all dataset against validation rules
}}

@index:
- api/link/ui.submenu_add.md
- api/link/ui.submenu_addcss.md
- api/link/ui.submenu_adjust.md
- api/link/ui.submenu_attachevent.md
- api/link/ui.submenu_bind.md
- api/link/ui.submenu_blockevent.md
- api/link/ui.submenu_callevent.md
- api/link/ui.submenu_clearall.md
- api/link/ui.submenu_clearcss.md
- api/link/ui.submenu_clearvalidation.md
- api/link/ui.submenu_close.md
- api/link/ui.submenu_copy.md
- api/link/ui.submenu_count.md
- api/link/ui.submenu_customize.md
- api/link/ui.submenu_define.md
- api/link/ui.submenu_destructor.md
- api/link/ui.submenu_detachevent.md
- api/link/ui.submenu_disable.md
- api/link/ui.submenu_disableitem.md
- api/link/ui.submenu_enable.md
- api/link/ui.submenu_enableitem.md
- api/link/ui.submenu_exists.md
- api/link/ui.submenu_filter.md
- api/link/ui.submenu_find.md
- api/link/ui.submenu_getbody.md
- api/link/ui.submenu_getchildviews.md
- api/link/ui.submenu_getfirstid.md
- api/link/ui.submenu_getformview.md
- api/link/ui.submenu_gethead.md
- api/link/ui.submenu_getidbyindex.md
- api/link/ui.submenu_getindexbyid.md
- api/link/ui.submenu_getitem.md
- api/link/ui.submenu_getitemnode.md
- api/link/ui.submenu_getlastid.md
- api/link/ui.submenu_getmenu.md
- api/link/ui.submenu_getmenuitem.md
- api/link/ui.submenu_getnextid.md
- api/link/ui.submenu_getnode.md
- api/link/ui.submenu_getpage.md
- api/link/ui.submenu_getpager.md
- api/link/ui.submenu_getparentview.md
- api/link/ui.submenu_getprevid.md
- api/link/ui.submenu_getscrollstate.md
- api/link/ui.submenu_getselectedid.md
- api/link/ui.submenu_getselecteditem.md
- api/link/ui.submenu_getsubmenu.md
- api/link/ui.submenu_gettopmenu.md
- api/link/ui.submenu_gettopparentview.md
- api/link/ui.submenu_getvisiblecount.md
- api/link/ui.submenu_hascss.md
- api/link/ui.submenu_hasevent.md
- api/link/ui.submenu_hide.md
- api/link/ui.submenu_hideitem.md
- api/link/ui.submenu_isenabled.md
- api/link/ui.submenu_isselected.md
- api/link/ui.submenu_isvisible.md
- api/link/ui.submenu_load.md
- api/link/ui.submenu_loadnext.md
- api/link/ui.submenu_locate.md
- api/link/ui.submenu_mapevent.md
- api/link/ui.submenu_move.md
- api/link/ui.submenu_movebottom.md
- api/link/ui.submenu_movedown.md
- api/link/ui.submenu_moveselection.md
- api/link/ui.submenu_movetop.md
- api/link/ui.submenu_moveup.md
- api/link/ui.submenu_parse.md
- api/link/ui.submenu_refresh.md
- api/link/ui.submenu_remove.md
- api/link/ui.submenu_removecss.md
- api/link/ui.submenu_render.md
- api/link/ui.submenu_resize.md
- api/link/ui.submenu_resizechildren.md
- api/link/ui.submenu_scrollto.md
- api/link/ui.submenu_select.md
- api/link/ui.submenu_selectall.md
- api/link/ui.submenu_serialize.md
- api/link/ui.submenu_setpage.md
- api/link/ui.submenu_setposition.md
- api/link/ui.submenu_show.md
- api/link/ui.submenu_showitem.md
- api/link/ui.submenu_sizetocontent.md
- api/link/ui.submenu_sort.md
- api/link/ui.submenu_sync.md
- api/link/ui.submenu_unbind.md
- api/link/ui.submenu_unblockevent.md
- api/link/ui.submenu_unselect.md
- api/link/ui.submenu_unselectall.md
- api/link/ui.submenu_updateitem.md
- api/link/ui.submenu_validate.md


