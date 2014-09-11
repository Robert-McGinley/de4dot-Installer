de4dot-Installer
================
Installer for [de4dot](https://www.github.com/0xd4d/de4dot) created by Robert McGinley ([robert.mcginley@gmail.com](mailto:robert.mcginley@gmail.com))

## Description ##
An installable package for the [de4dot](https://www.github.com/0xd4d/de4dot) .NET deobfuscator for Windows.
Binary version of [de4dot](https://www.github.com/0xd4d/de4dot) & dnlib compiled under *Visual Studio 2013*.

***Please see the [Issues section](https://github.com/Robert-McGinley/de4dot-Installer/issues) to weigh-in on future developments of this project!*** I need input from you!

I intend to keep the installer(s) up to date with de4dot releases and perhaps even provide builds from the *master* branch from time-to-time. Currently the installer is created with *Caphyon Advanced Installer*; However I intend to migrate to a pure WIX installer at some point.

The installer supports *Windows XP* and greater as long as a minimum of *.NET 2.0* is installed. ***Whether de4dot will work on older platforms or not has not been tested, nor will it be. YMMV.*** 

Currently, de4dot-Installer is created with *Advanced Installer v10.6* Visual Studio plugin. A pure MSI/WIX installer is planned for the future.

## Features ##

By default the installer provides the following:
- 32bit and 64bit de4dot binary components
- Windows Start Menu shortcuts
	- Open the de4dot installation directory
	- Open a command prompt under the de4dot installation directory (using de4dot_shell.bat)
	- Links to the de4dot and de4dot-Installer GitHub pages
	- Links to de4dot README (Text, RTF and PDF versions)
	- Links to license files for software included in de4dot
	- Links to de4dot license files (Text & RTF versions)
- Windows Explorer Context Menu items for .exe and .dll files
	- "Deobfuscate with de4dot"
- Repair/Modify/Uninstall support
 
## Explorer Context Menu Entries ##
To delete or modify the Explorer Context Menu Entries, open a registry editor (such as `regedit.exe`) and navigate to `HKEY_CLASSES_ROOT\dllfile\shell\de4dot` and/or `HKEY_CLASSES_ROOT\exefile\shell\de4dot`.

As long as you know what you're doing, modify or delete to your hearts content.

# Changelog #

- **8/31/2014** - Initial Installer build committed
- **9/10/2014** - Added compiled binary 7Zip archive of de4dot v3.1.41592/dnlib v1.0.2
	- This is for those who want the binaries, but not the installer, shortcuts or explorer right-click integration stuff.
- **9/10/2014** - Added installer for latest de4dot-master commit (Commit [42682d0fae](https://github.com/0xd4d/de4dot/commit/42682d0fae5cdc507b642223d5714dbaf83070a8), added July 25th 2014). 
	- Titled de4dot v3.1.41592.3405 Unstable to differentiate from the actual v3.1.41592 release.
	- I wouldn't consider this "Unstable", as it's worked flawlessly for me. However *YMMV*
- **9/11/2014** - Added compiled binary 7Zip archive of de4dot v3.1.41592.3405/dnlib 1.0.2.0 (From de4dot-master & dnlib-master projects as-of 9/1/2014)
	- These are the same binaries & PDBs that are provided in the v3.1.41592.3405 Unstable installer for those who just want de4dot and not the installer & fluff
	- All caveats from using the aforementioned installer still apply. No modifications have been made to the de4dot or dnlib source.
	- Compiled under Visual Studio 2013

# TODO #
- Separate the de4dot x86 & x64 components into individual packages
- Build a GUI for de4dot in C# (Would be another project but likely included in this one)
- Migrate the Advanced Installer build configurations to pure WIX installer configurations
- Provide .NET CLR version specific builds (Is this even feasible or necessary?)
- **What would you like to see?**
