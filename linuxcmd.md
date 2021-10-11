##  What does “{} \;” mean in find (in Linux)?
> it's a placeholder for each file that the find command locates (taken from here). \
> sefacl is a special command which used to set beyond non-group user accessing the file system \
> suppose user mostain is not in a member of devops group but still we can allow him to access certain file or folder.

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
