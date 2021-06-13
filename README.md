# Linux Commands

## Info (List all the available command info )
> `$ info`

## which command gives the command location / source path
`$ which ls`

> output:
> /usr/bin/ls

## Hard link
[Link Guide](https://www.computerhope.com/unix/uln.htm) \

``$ link fileExist.txt newLinkFile.txt``

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
`$ls -p | grep -v /` \

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
- \* means executable.
- = means socket.
- | means named pipe.
- \> means door.
- / means directory.

> `ls -F | grep -Ev '/|@|*|=|\|'`

> `ls -F | grep -Ev '/|@|*|=|>|\|'`

## How to get package info (using package manager dpkg)
`$ whatis dpkg`

`$ which column`

`$ dpkg -S $(which column)`

## Check the ip address
`$ ip address`

## Deafult permission | umask command

### Default File Permission
* Files: rw-rw-rw- (666)
* Directories: rwxrwxrwx (777)

#### Get the umask value
>`$ umask`

>Lets assume your umask value is **002** \
>octal to binary to mode \
>002 --> 010 --> -w- 

> Now create a file called: student.txt \
> Calculate the mode value beforehand: \
> rw- rw- rw- \
> --- --- -w- \
> ---------------- \
> rw- rw- r-- ==> 664

> Now check the student.txt file permssion using ls -l or stat command
`$ stat student.txt`
>

# Concatenate Command -cat
> It reads data from the file  and gives their content as output. It helps us to create, view, concatenate files

> `cat > file1.txt
 master-academy
 to save and close use ctrl+d
 <newline feed>
`
> `cat -n file1.txt`
> show content with line numbers

> `cat file1.txt > file2.txt` overright one file by another

> `tac file1.txt` content display in reverse order

> `cat file1.txt file2.txt` view content from multiple files

> `cat file1.txt file2.txt > file3.txt` combines multiple files output into a new file

> `cat file1.txt >> file2.txt` to append the file1.txt to file2.txt

> `cat file1.txt | cat >> other.txt` pipeing one file output appending into other file



### References:
* [Hard link](https://www.cyberciti.biz/faq/how-to-find-all-hard-links-in-a-directory-on-linux/)
* [LS Display](https://askubuntu.com/questions/811210/how-can-i-make-ls-only-display-files)
* [Unmask](https://www.youtube.com/watch?v=JYT7y_Pe9wE)
