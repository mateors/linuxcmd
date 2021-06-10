# Linux commands

## Print info
> `info`

## Hard link
[Link Guide](https://www.computerhope.com/unix/uln.htm)
`$ link fileExist.txt newLinkFile.txt`
* The file name and the file's data are two separate entities.
![link illustration](https://www.computerhope.com/unix/images/nolink-diagram.jpg)

## List all files including inode
> `$ ls -li`

## How to find all hard links to a given file / Find out all hard links of inode 531188
> `$ find / -inum 531188`

## Gives a list of all files which have more than one link.
> `$ find . -type f -links +1 2>/dev/null`

## How can I make ls only display files?
### Method-1
`$ls -p | grep -v /`
`$ls -p | grep -v / | column`
> Using ls -p tells ls to append a slash to entries which are a directory, and using grep -v / tells grep to return only lines not containing a slash.

- p adds the forward slash ('/') to the directory names
- r reverses the order of output
- v lets grep do an inverse search to print everything except the directories (everything that doesn't have the '/' that -p put there)
- column puts it in columns


### Method-2
`find . -maxdepth 1 -not -type d`

### Method-3
`ls -p | egrep -v /$`

### Method-4
`ls -F | grep -v /`
> Above command displays files, But it includes symlinks, pipes, etc. If you want to eliminate them too, you can use one of the flags mentioned below.

ls -F appends symbols to filenames. These symbols show useful information about files.

- @ means symbolic link (or that the file has extended attributes).
- * means executable.
- = means socket.
- | means named pipe.
- > means door.
- / means directory.

> `ls -F | grep -Ev '/|@|*|=|\|'`
> `ls -F | grep -Ev '/|@|*|=|>|\|'`

## How to get package info (using package manager dpkg)
`$ whatis dpkg`
`$ which column`
`$ dpkg -S $(which column)`



