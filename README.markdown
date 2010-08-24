Build mode helper
=================

This module creates common sense themes for custom build modes that you create
by implementing `hook_content_build_modes()`.

Usage
-----

There is no administrative UI for this module, so you must create build modes
by implementing `hook_content_build_modes()` in your custom module or use this
module to theme build modes provided by other modules.

`buildmode_node_view()` is a substitute for core `node_view()` but takes a
build mode as an argument instead of teaser and page.

The module provides node reference field formatters for each of your custom
build modes. This extends node reference field formatters beyond *title (link)*,
*title (no link)*, *full* and *teaser*. For example, if you have a story node
with a node reference field to link a person node, you can format that node
reference field with an *author* build mode that you implement.

Any build mode can be themed using a custom template named for the build mode
or the build mode and the node type. For example, if the build mode is named
*figure*, your template suggestions for an image node in that build mode will
include:

* node.tpl.php
* node-image.tpl.php
* figure.tpl.php
* figure-image.tpl.php

The module implements `hook_menu()` to expose a callback for viewing nodes in
different build modes.
