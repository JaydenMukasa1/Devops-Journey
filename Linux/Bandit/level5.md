Level 5 → 6

Task


Solution
Used ls to view the home directory, cd to enter inhere, then ran find . ! -executable -readable -size 1033c to locate the  file. It gave one result, then I used cat to reveal the password.
! means “not”, and you can also use -readable, -executable, and -writable with find to filter files.


Key Commands 
ls
cd
cat
find
