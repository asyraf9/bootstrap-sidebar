bootstrap-sidebar
=================

A responsive sidebar plugin for bootstrap 3. if your menus are too big to fit into a horizontal menubar, or you need to have a responsive sidebar that is compatible with bootstrap, then this is the plugin for you. 

Features:
1. on mobile sized screens, the sidebar becomes a slide in menu
2. You can set the sidebar size for each screen size using standard bootstrap grid classes
3. hardware accelerated slide-in animation.

Current Limitations: 
1. This sidebar assumes you have a fixed top menubar
2. This plugin is only tested for the left sidebar only. support for setting up a right sidebar exists but has never been tested yet. 
3. Clicking outside the sidebar does not close the sidebar in smaller screens.
4. On larger screens the sidebar is open(visible) by default and there is no way to change this at the moment. 
5. you will have to write some custom css to enable fixed horizontal menu items

Demo:
checkout the Plunker here: http://plnkr.co/edit/vUoQOe?p=preview

Usage:
Usage is almost the same as the horizontal menubar collapse method: define a button on your top menubar that toggles the sidebar on and off like this:

```html
<button type="button" class="navbar-toggle" data-toggle="sidebar" data-target=".sidebar">
  <span class="sr-only">Toggle navigation</span>
  <span class="icon-bar"></span>
  <span class="icon-bar"></span>
  <span class="icon-bar"></span>
</button
```

Note the data-toggle and data-target attriubutes - these are the attributes necessary to make this button work with sidebar

then define your sidebar column as:

```html
<div class="col-xs-7 col-sm-3 col-md-2 sidebar sidebar-left sidebar-animate sidebar-closed">
  <!-- content -->
</div>
```

Note the important classes: 

"sidebar" - main css class
"sidebar-left" - to define the position of your sidebar and slide-in slide-out animations
"sidebar-animation" - to tell sidebar to animate sliding in and out. Leave this out to disable animation
"sidebar-closed" - this tells the sidebar to be closed by default on smaller screens. It is automatically open by default on larger screens
"col-xs-7", "col-sm-3", "col-md-2" - you can freely set the column size across different screen sizes according to Bootstrap's Grid guidelines

