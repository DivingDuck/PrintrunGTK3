Pronterface-Projector GTK-3 add-on files for Windows 10 x32/x64
===============================================================

Status WIP

This repository will become a submodule of [Printrun](https://github.com/kliment/Printrun) and include Windows specific GTK-3 binaries that are needed for running the module Projector.

## Binaries for Windows 10 x64
The files are extracted from the GTK+ for Windows Runtime Environment that is based on repository https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer by Tom Schoonjans. 
This repository will include only DLL files needed by cairocffi and cairosvg. The files are not modified. 

Source of files: 
[gtk3-runtime-3.24.24-2021-01-30-ts-win64](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases/download/2021-01-30/gtk3-runtime-3.24.24-2021-01-30-ts-win64.exe)

## Binaries for Windows 10 x32
The files are extracted from the GTK+ for Windows Runtime Environment that is based on Tarnyko's http://www.tarnyko.net/dl/gtk.htm
This repository will include only DLL files needed by cairocffi and cairosvg. The files are not modified.

Source of files:
[gtk+-bundle_3.6.4-20130513_win32](http://www.tarnyko.net/repo/gtk3_build_system/gtk+-bundle_3.6.4-20130513_win32.zip)

## How to use

You can build Pronterface with or w/o these binaries. In addition you need
different binaries depending if you build a Windows 10 x32 or x64 version.

Download and copy the directory PrintrunGTK3 manually in the root of the [Printrun](https://github.com/kliment/Printrun) Project source code or clone
the included submodule via: 

git submodules --recursive

There will exist soon an updated a batch file called release_windows.bat within project
 [Printrun](https://github.com/kliment/Printrun) that build an executable version what
 includes instructions how to build Pronterface for Windows 10 as x64 or x32 version
 with or w/o GTK3 bundled. Follow the instruction in the batch script and activate the
 version you want to build. By default the batch will build a x64 bit version with GTK bundled.

You can also find a first preview version in my repository. Checkout branch [Test](https://github.com/DivingDuck/Printrun/tree/test)

WIP, to be continued ...
