## How to install any application using command line?
There are two way of doing this using the command line
To install any package, just open a terminal ( Ctrl + Alt + T ) and type sudo apt-get install <package name> 
  
### Software repositories
Repository is a place where software is stored

### What is package?
Files associated with a package management system. Every Linux distribution comes with a package management system, but they are not all the same.
  
The most common method of installing apps from the command line is through software repositories using what's called a package manager. All Linux apps are distributed as packages.
  
Syntax for installing deb-files

> sudo apt install path_to_deb_file

> sudo dpkg -i path_to_deb_file

example:
> sudo apt install ./code_1.64.2-1644445741_amd64.deb


## Resource
* https://itsfoss.com/install-deb-files-ubuntu/
* https://opensource.com/article/18/8/how-install-software-linux-command-line
