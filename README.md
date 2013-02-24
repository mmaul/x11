NAME: x11

VERSION: .02  

AUTHOR: Mike Maul

AUTHOR_EMAIL mike d0t maul [at] gmail <.> com

PKG_URL: https://github.com/mmaul/x11

DESCRIPTION: X11 bindings

CATEGORY: GUI

LIBDIR: X11

-----

X11 system interface and examples
---------------------------------

Files
-----
X11/x11.flx       - X11 interface
config/x11.fpc    - x11 flx_pkgconfig file
examples/hello_world.flx   - Simple example
examples/tinyflxwm.flx     - Implementation of Nick Welch's  tinywm (http://incise.org/tinywm.html) 
		    the 50 line window manager in felix with verbose formatting 
                    and comments
examples/min_tinyflxwm.flx - Implementation of tinyflwm the 50 line window manager in 
                    felix in 50 lines

Running
-------

  To run the example hello_world
    flx hello_world
  * in BSD you need to supply -L/usr/local/lib arg to flx like
    flx -L/usr/local/lib hello_world

  * on OSX and probably most Linux platforms, you will need to supply
    the linker switch -L/usr/X11/lib so the x11 library can be found
    by the linker

  tinyflxwm
  ---------
  To run the window manager examples first start a nested display with
    Xnest :10
  Then pass the DISPLAY of the X server to tinyflxwm
    DISPLAY=:10.0 flx tinyflxwm
  And of course you need a window to manage, so lets try xclock
    DISPLAY=:10.0 xclock
  Usage:
    Grab with Shift-Alt-MouseButton-1
    Move with Shift-Alt-MouseButton-2

Installing
----------
flx setup install
