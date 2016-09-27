# clockutc
*a simple clock that shows utc time for Windows, written in Qt/C++*

![alt text](https://github.com/isc1/clockutc/blob/master/clockutc-screenshot.jpg "clockutc")

This clock is really just the DigitalClock code example included with Qt &
Qt Creator ( http://doc.qt.io/qt-5/qtwidgets-widgets-digitalclock-example.html )
with a few lines changed so that it shows UTC (Universal Time Coordinated:
https://en.wikipedia.org/wiki/Coordinated_Universal_Time ).

A .zip file containing the executable is included if you don't want to build it.
Just unzip the contents to somewhere like

- C:\Program Files\Utils\

...your antivirus software might complain; if that makes you uncomfortable, do
not run clockutc.exe from the .zip file, but inspect the code and build it yourself.

If you want to build it yourself, and you then want to pin it to the windows taskbar
to run it (for example), you can copy the executable to somewhere like:

- C:\Program Files\Utils\clockutc.exe

...and then copy the following files to that directory also:

- Qt5Core.dll
- Qt5Gui.dll
- Qt5Widgets.dll

...otherwise, when you try to run clockutc.exe, windows will give you error pop-ups
saying things like, "The program can't start because Qt5Core.dll is missing from your
computer".

Qt includes several different versions of these files.  Depending on what version you
are running, that will determine which copies of those files you need.  If you don't
copy the .dll files from the .zip file, and build clockutc.exe yourself, then after
you have opened the project in Qt Creator, see:

- Tools > Options > Build & Run > Qt Versions

The folder containing the .dll files you need will probably look like:

- C:\Qt\5.7\msvc2015_64\bin

...this is all because, by default, Qt builds with dynamic linking.

This code runs okay on Windows 10 with Qt 5.7.0, and should work on linux and
Mac OS X too, but I haven't built it on those platforms yet.  If you have
changes that will get it to run on linux & Mac, I will look at pull requests. :)