# clockutc
*a simple clock that shows utc time, written in Qt/C++*

This clock is really just the DigitalClock code example included with Qt &
Qt Creator with a few lines changed so that it shows UTC (Universal Time
Coordinated  https://en.wikipedia.org/wiki/Coordinated_Universal_Time ).

This code runs okay on Windows 10 with Qt 5.7, and should work on linux and
Mac OS X too, but I haven't built it on those platforms yet.  If you have
changes that will get it to run on linux & Mac, I will look at pull requests. :)

To get this to run on windows from the taskbar, you can copy the executable
to something like
- C:\Program Files\Utils\clockutc.exe
...and then copy the following files to that directory also:

- Qt5Core.dll
- Qt5Gui.dll
- Qt5Widgets.dll

...depending on what version compiler you are running, that will determine
which copies of those files you need.  In Qt Creator, after you open the
clockutc project, see: Tools > Options > Build & Run > Qt Versions

...or you can look in the file clockutc.pro

The folder containing the .dll files you need will probably look like:

C:\Qt\5.7\msvc2015_64\bin

...this is all because, by default, Qt builds with dynamic linking.