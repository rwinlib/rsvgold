Experimental support for rsvg on Windows.

Dependencies glib2 and gdk-pixbuf2 do not support static linking,
therefore we need to ship a ton of dependencies. Also doesn't work
well on win32 with the new tool chain.