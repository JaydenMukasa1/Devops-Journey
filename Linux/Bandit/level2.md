Level 2 → 3

Task
Find the password for the next level in a file called --spaces in this filename-- located in the home directory.

Solution
To access files with spaces in them, you can wrap the filename in quotes or escape the spaces with backslashes.
This file also starts with --, which makes Linux think it is an option, so we add -- before it to tell Linux it is a normal file.

cat -- "--spaces in this filename--"

Commands Used
ls
cat
