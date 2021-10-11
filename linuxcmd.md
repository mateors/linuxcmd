##  What does “{} \;” mean in find (in Linux)?
> it's a placeholder for each file that the find command locates (taken from here). \

## Why setfacl while we have chmod, chown & sticky bit?
> sefacl is a special command which used to set beyond non-group user accessing the file system \
> suppose we have a file called **record.txt** user **wania** is the owner of the file and is under **devops** group. \
> Another user **mostain** who is not a member of the **devops** group \
> But still we want allow him to access **record.txt** file with write permission. \
> We can not achive this using builtin file permission, in this scneario we can use **setacl** to achive our requirements.


## setfacl && getfacl
>  setfacl command sets file access control lists. \
> getfacl gets the file access information

> setfacl -m u:mostain:rwx file1.txt \
> setfacl -m g:devops:r-x file1.txt

## Modifying multiple directory in a single command
> setfacl -R -m u:sanzida:rX /home/mostain/{live,tutorial}

## Show the current ACL
> getfacl file1.txt

## Revoke write access from all groups and all named users. (m=umask)
> setfacl -m m::rx file1.txt

# Reference
* https://www.computerhope.com/unix/usetfacl.htm
