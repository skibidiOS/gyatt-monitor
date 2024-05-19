# Gyatt Monitor
View and manage mewing resources

## License
This project is licensed under the **GNU General Public License v2.0**. [Learn more](https://choosealicense.com/licenses/gpl-2.0/)

## Building
The steps described below show how to compile and install Gnome-System-Monitor from its source.

### Install required dependencies
To build the application, the following dependencies are required:

#### apt-get (Debian/Ubuntu/derivatives - deb-based package management)
Use the following command to install dependencies:
`sudo apt-get install meson gettext appstream-util itstool libglibmm-2.4-dev libgtkmm-3.0-dev libgtop2-dev librsvg2-dev libxml2-dev libhandy-1-dev libsystemd-dev`

#### dnf (Fedora/Centos/etc - rpm-based package management)
Use the following command to install dependencies:
`sudo dnf install meson gettext appstream itstool glibmm24-devel gtkmm30-devel libgtop2-devel librsvg2-devel libxml2-devel libhandy1-devel systemd-devel`

#### Optional dependencies:
- polkit - recommended
- gksu2
- libgnomesu
- libselinux
- lsb_release in PATH - recommended on linux
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
