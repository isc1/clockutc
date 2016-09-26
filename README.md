# clockutc
*a simple clock that shows utc time, written in Qt/C++*

This clock is really just the demo clock included with Qt & Qt Creator with a few
lines changed.

To get this to run on windows from the taskbar, you can copy the executable
to something like C:\Program Files\Utils\clockutc.exe
...and then copy the following files to that directory also:

Qt5Core.dll
Qt5Gui.dll
Qt5Widgets.dll

...depending on what version compiler you are running, that will determine
which copies of those files you need.  In Qt Creator, after you open the
clockutc project, see: Tools > Options > Build & Run > Qt Versions

...or you can look in the file clockutc.pro

The folder containing the .dll files you need will probably look like:

C:\Qt\5.7\msvc2015_64\bin

...this is all because, by default, Qt builds with dynamic linking.  If they
just defaulted to static linking, you would have one nice, self-contained .exe
file (although it would be bigger) and thousands of people wouldn't have to
waste time with this .dll copying hassle for little projects like this.  But
whatever.