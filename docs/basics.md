# Basic Usage of MX Fluxbox

## What is Fluxbox?

Fluxbox is a [Window Manager](https://en.wikipedia.org/wiki/Stacking_window_manager) (unlike Xfce, which is a Desktop Environment) that controls the placement and appearance of windows.  For history and overview, consult the [Wikipedia](https://en.wikipedia.org/wiki/Fluxbox).

## How do I get started?

- Use the desktop menu: right-click anywhere on the desktop. This menu is restricted to 1) common apps, 2) fluxbox settings and 3) session actions. It is set by ~/.fluxbox/menu-mx. 
- Use the default toolbar at the top.
- The user can see the entire MX-Xfce Application Finder by clicking “All apps” in the desktop menu, pressing F6, or clicking the MX Linux icon on the top of the dock on the left side of the screen.

## What is the toolbar across the top?

![Fluxbox Toolbar](toolbar.png)

This fluxbox toolbar offers MX users information about workspaces, open applications, a system tray, and the current time. Its width and placement can be set with the options available by middle-clicking (=scroll wheel) the clock or pager on the toolbar—if that doesn’t work for some reason, click Menu > Settings > Window, slit and toolbar > Toolbar. Height is set in ~/.fluxbox/init/ :

session.screen0.toolbar.height:   0	

If a zero is there, it means that the selected style will set the height. Otherwise, a value of 20 to 25 is often comfortable.

The toolbar contains the following default components (L-R):

- pager 

Allows you to switch workspace up (right click) or down (left click); same as Control + F1/F2/ etc., Ctrl-Alt + ←/→ or using the scroll wheel over an empty section of the desktop. Number and name are set in the ~/.fluxbox/init. “W” stands for “Workspace.”

- iconbar 

Here open apps will show an icon, with various window options available by right-clicking the relevant icon (including the toolbar itself) > iconbar mode.  Default for MX-Fluxbox is All Windows. 

- systemtray AKA systray

Equivalent of Notification Area in Xfce. Default components set in ~/.fluxbox/init; apps that have a systemtray option will show there when launched.  

- clock 

To adjust the clock to 12h or 24h, right-click and click 12h or 24h, whichever shows. If that doesn’t work, select "Edit clock format." 
-- 24h: %H:%M, 12h: %I:%M.
-- The default is 12h time and date in day/short month format: %I:%M  %b %d. Many other time/date options are available: https://mxlinux.org/wiki/other/time-formats-in-scripts/ 

You can move or delete any of the toolbar components in ~/.fluxbox/init/ , which by default are set up in this way:

	workspacename, iconbar, systemtray, clock 

