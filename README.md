Show Maya shelves as menus.

![](https://s3.amazonaws.com/zewt/zShelfMenu+screenshot.png)

Maya shelves are handy, but they quickly become unmanagable, since they can only show 6-letter labels.
This plugin shows shelves as Maya menus.

By default, a "Shelves" menu item will be added, which contains a submenu for each shelf.
The full name of each shelf button is used, so you can use descriptive names for each menu
item.

Selecting "Show on shelf" at the bottom of any shelf menu will add the menu directly to the
main menu to make it quick to select.

The options box on each shelf item will open it in the shelf editor for quick editing.

Shelf menus can be torn off like other menus, and shelf popup menus will be displayed in submenus.

Usage
-----

Copy **zShelfMenu.mod** into Maya's modules directory, setting the path to the location
of zShelfMenu.  In plugin manager, enable zShelfMenu.py.

Notes
-----

Shelf scripts won't be printed to the script console each time they're run, like they are
when a shelf button is clicked.  This reduces output clutter.

Limitations
-----------

If a shelf item has both a script and popups, only the popups will be available.

Torn-off shelf menus won't automatically update if the shelf is modified.

If the name of a shelf is changed, it will be lost from the list to show as a top-level
menu.

If a submenu of the Shelves menu is torn off, it'll disappear if the Shelves menu is opened.
This is a Maya limitation and affects built-in menus as well, like Deform submenus.  It doesn't
affect top-level menus.

Python code will be called with an empty environment.  Shelves are normally executed in a shared
global environment, but I'm not sure how to get access to it.  (This is messy: it means shelf
scripts with missing imports will work if they're used after a script that imports it, but not
if you use it first, so it's best to fix these anyway.)

