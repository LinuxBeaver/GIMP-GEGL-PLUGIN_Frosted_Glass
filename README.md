# Ice Text - Ice cold text with dripping icicles

Create ice dripping frozen text effects with this GIMP plugin, 

![image](https://github.com/user-attachments/assets/d868a314-6290-494c-b104-e29ff5a1c413)


## Directory to put Binaries (They do NOT go in the normal plugins folder)

**Windows**

 C:\Users\(USERNAME)\AppData\Local\gegl-0.4\plug-ins

 **Linux**

~/.local/share/gegl-0.4/plug-ins

 **Linux (Flatpak includes Chromebook)**

~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins

Then Restart Gimp and go to Filters>Text Styling and look for "Frozen Gel" or just search for it with /

GIMP 2.10 users will only find this in GEGL Operation drop down list and it will only work on 2.10 if they are using GEGL 0.4.50+, all normal windows builds of GIMP 2.10 ship with GEGL 0.4.48

## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```

### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

btw this plugin has a sister plugin named Frozel Gel
https://github.com/LinuxBeaver/GIMP-GEGL-PLUGIN_Frozen_Gel/

