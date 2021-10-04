# Special commands
Specially use in bash script

## The number of arguments
**$#** is the number of arguments, but remember it will be different in a function. $# is the number of positional parameters passed to the script, shell, or shell function. This is because, while a shell function is running, the positional parameters are temporarily replaced with the arguments to the function.

## What does $@ mean in shell?
**$@** refers to all of a shell script's command-line arguments. $1 , $2 , etc., refer to the first command-line argument, the second command-line argument, etc. Place variables in quotes if the values might have spaces in them.
