## How to install any application using command line?
There are two way of doing this using the command line
To install any package, just open a terminal ( Ctrl + Alt + T ) and type sudo apt-get install <package name> 
  
### Software repositories
Repository is a place where software is stored

### What is package?
Files associated with a package management system. Every Linux distribution comes with a package management system, but they are not all the same.
  
The most common method of installing apps from the command line is through software repositories using what's called a package manager. All Linux apps are distributed as packages.
 
### What is Dependency?
What other apps it may depend on
  
## What is Package management system?
A package management system is comprised of sets of tools and file formats that are used together to install, update, and uninstall Linux apps.
  
> The most common package management systems are .deb .rpm .tar
  
* Red Hat, CentOS, and Fedora all use the rpm system (.rpm files)
* Debian, Ubuntu, Mint use dpkg (.deb files)
* Arch Linux uses nothing but tarballs (.tar files)
* Gentoo Linux uses a system called Portage
  
## What's inside an .rpm, .deb, or .tar file?
Nothing more than plain old archive files (like .zip) that contain an application's code, instructions on how to install it, dependencies , and where its configuration files should be placed. The software that reads and executes all of those instructions is called a package manager.
  
## What is Package manager?
A package manager keeps track of what software is installed on your computer, and allows you to easily install new software, upgrade software to newer versions, or remove software that you previously installed.

## DPKG
Stands for Debian package. It is the default package manager on Ubuntu. **Debian-based distributions** all use .deb files and the **dpkg** package management system. **dpkg** is a command line way to install from a **.deb** or remove already installed packages.
  
## APT
* [Advanced Package Tool or APT](https://wiki.debian.org/Apt)
  
Syntax for installing deb-files

> sudo apt install path_to_deb_file

> sudo dpkg -i path_to_deb_file

example:
> sudo apt install ./code_1.64.2-1644445741_amd64.deb


## Resource
* https://itsfoss.com/install-deb-files-ubuntu/
* https://opensource.com/article/18/8/how-install-software-linux-command-line
