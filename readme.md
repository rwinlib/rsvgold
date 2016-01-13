Experimental support for rsvg on Windows.



Currently glib2 does not support support static linking because it 
uses DllMain hooks for initiation. Therefore we ship glib2 and its
dependencies as DLL files.

Build Notes:
 - glib2 was recompiled with --threads=win32
 - renamed DllMain from gdk-pixbuf2 (we dont need DllMain).
 - gdk-pixbuf2 needs patch from mingw-packages to enable static.
 - libcairo also seems to have DllMain

With the experimental toolchain sometimes the package installation 
freezesin win32 at "testing if installed package can be loaded". 
However if we install with --no-test-load the package works fine. 
Have to further investigate this. 
