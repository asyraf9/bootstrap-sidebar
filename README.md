Changelog:
v0.1.0
1. Right sidebar now fully tested. make sure your right sidebar is after your 'main' content in your HTML if you want to make it a permanent sidebar at any screen size.
2. Clicking anywhere outside of the sidebar hides the sidebar (if it is not set to permanent) see index.html
3. sidebars are now hidden by default, and you can override it by adding a sidebar-show-<size> class (replace size with xs, sm, md, lg as per Bootstrap's convention) see index.html

bootstrap-sidebar
=================

A responsive sidebar plugin for bootstrap 3. if your menus are too big to fit into a horizontal menubar, or you need to have a responsive sidebar that is compatible with bootstrap, then this is the plugin for you. 
(NOTE: Contributions are welcome! please issue a Pull Request. I'll include tests soon, please include tests in your code as well!)


Features:

1. on mobile sized screens, the sidebar becomes a slide in menu
2. You can set the sidebar size for each screen size using standard bootstrap grid classes
3. hardware accelerated slide-in animation.

Current Limitations: 

1. This sidebar assumes you have a fixed top menubar
2. ~~This plugin is only tested for the left sidebar only. support for setting up a right sidebar exists but has never been tested yet.~~ 
3. ~~Clicking outside the sidebar does not close the sidebar in smaller screens.~~
4. ~~On larger screens the sidebar is open(visible) by default and there is no way to change this at the moment.~~ 
5. you will have to write some custom css to enable fixed horizontal menu items

Demo:
checkout the Plunker here: http://plnkr.co/edit/vUoQOe?p=preview

New v0.1.0 coming soon. 

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
<div class="col-xs-7 col-sm-3 col-md-2 sidebar sidebar-left sidebar-animate sidebar-show-md">
  <!-- content -->
</div>
```

Note the important classes: 

* "sidebar" - main css class
* "sidebar-left" - to define the position of your sidebar and slide-in slide-out animations. Options are: sidebar-left, sidebar-right
* "sidebar-animation" - (Optional) to tell sidebar to animate sliding in and out.
* "sidebar-open-md" - (Optional) tells the sidebar to be permanently open. 'md' denotes the screen size you want the sidebar to be permanently open at (options are: xs, sm, md, lg). make sure you set your column sizes accordingly to accomodate a permanent sidebar. 
* "col-xs-7", "col-sm-3", "col-md-2" - you can freely set the column size across different screen sizes according to Bootstrap's Grid guidelines

