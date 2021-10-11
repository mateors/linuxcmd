##  What does “{} \;” mean in find (in Linux)?
> it's a placeholder for each file that the find command locates (taken from here).

## setfacl && getfacl
>  setfacl command sets file access control lists. \
> getfacl gets the file access information

> setfacl -m u:mostain:rwx file1.txt \
> setfacl -m g:devops:r-x file1.txt

## Show the current ACL
> getfacl file1.txt

## Revoke write access from all groups and all named users. (m=umask)
> setfacl -m m::rx file1.txt

# Reference
* https://www.computerhope.com/unix/usetfacl.htm
