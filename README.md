# System Monitor
GNOME System Monitor is a GNOME process viewer and system monitor with an attractive, 
easy-to-use interface, It has features, such as a tree view for process dependencies,
icons for processes, the ability to hide processes that you don't want to see,
graphical time histories of CPU/memory/swap usage,
the ability to kill/renice processes needing root access,
as well as the standard features that you might expect from a process viewer.

## License
This project is licensed under the **GNU General Public License v2.0**. [Learn more](https://choosealicense.com/licenses/gpl-2.0/)

## Building
The steps described below show how to compile and install Gnome-System-Monitor from its source.

### Install required dependencies
To build the application, the following dependencies are required:

Debian/Ubuntu: `sudo apt-get install meson gettext appstream-util itstool libglibmm-2.4-dev libgtkmm-3.0-dev libgtop2-dev librsvg2-dev libxml2-dev`

Optional dependencies:
- libgksu2 - recommended
- libgnomesu
- libselinux
- lsb_release in PATH - recommended on linux
- libsystemd-dev
- libwnck

### Building and installing
Before following the steps below, clone the repository and change to its working directory.

##### Configure and create the build directory with Meson.
`meson build`

Where `build` is just a directory name, and is up to your chosing.
##### Build the application - this compiles the source.
`ninja -C build`
 
##### Install the application on your system - required to run Gnome-System-Monitor.
`ninja -C build install`

### Cleanup

##### Use the following command to clean up the build directory and remove old build files.
`ninja -C build -t clean`

##### Remove the build directory to rebuild from scratch.
`rm -rf build`

## Bugs

Please file System-Monitor bugs at:
https://gitlab.gnome.org/GNOME/gnome-system-monitor/issues