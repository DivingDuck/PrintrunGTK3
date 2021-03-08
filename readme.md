Pronterface-Projector GTK-3 add-on files for Windows 10 x32/x64
===============================================================

This repository supports [Printrun](https://github.com/kliment/Printrun) with a 
submodule of additional needed files for the Projector interface. It includes 
a selection of Windows specific GTK-3 DLL binaries.

## Binaries for Windows 10 x64
These files are extracted from the GTK+ for Windows Runtime Environment that is based on repository https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer by Tom Schoonjans. 
This repository will include only DLL files needed by cairocffi and cairosvg. The files are not modified. 

Source of files: 
[gtk3-runtime-3.24.24-2021-01-30-ts-win64](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases/download/2021-01-30/gtk3-runtime-3.24.24-2021-01-30-ts-win64.exe)

## Binaries for Windows 10 x32
These files are extracted from the GTK+ for Windows Runtime Environment that is based on Tarnyko's http://www.tarnyko.net/dl/gtk.htm
This repository will include only DLL files needed by cairocffi and cairosvg. The files are not modified.

Source of files:
[gtk+-bundle_3.6.4-20130513_win32](http://www.tarnyko.net/repo/gtk3_build_system/gtk+-bundle_3.6.4-20130513_win32.zip)

## How to use

You can build Pronterface with or w/o these binaries. In addition you need
different binaries depending if you build a Windows 10 x32 or x64 version.

There are tree ways how you can use these binaries:

* Download and copy the directory PrintrunGTK3 manually in the root of the [Printrun](https://github.com/kliment/Printrun) project source code
* clone an included submodule where you miss the files: 

    `git submodules --recursive`

  In case the submodule is not already integrated in the project you can add the module this way:

    ```git submodule add https://github.com/DivingDuck/PrintrunGTK3```
    ```git submodule update --init --recursive```

  In case you need to update the submodule to the latest version:

    `git submodule update --remote`

* Download and copy the files to an location and place of your choice manually
  and make the path to the binaries available by adding this path to 
  windows environment variable path. Like:

  for x64 version: `path = c:\GTK3Windows10-64\bin`

  for x84 (32 bit) version: `path = c:\GTK3Windows10-32\bin`

  Don't mix or combine the files for running Pronterface in 32 bit or 64 bit,
  this won't work.

There may exist in the future an updated batch file called release_windows.bat within
 the [original project Printrun](https://github.com/kliment/Printrun) that build an executable
 version what includes instructions how to build Pronterface for Windows 10 as
 x64 or x32 version with or w/o GTK3 bundled. Follow the instruction in the file
 and activate the version you want to build. By default this batch will build
 a x64 bit version with GTK bundled.

You can also find an updated version of [release__windows.bat](https://github.com/DivingDuck/Printrun/blob/master/release_windows.bat)
 in my repository [Printrun](https://github.com/DivingDuck/Printrun) if needed.
 Copy the file in the root of your printrun project and let it do it's work.
