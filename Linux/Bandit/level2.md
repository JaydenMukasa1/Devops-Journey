Level 2 → 3

Task
Find the password for the next level in a file called --spaces in this filename-- located in the home directory.

Solution
To access files with spaces in them, you need to wrap the file name in quotations.
E.g
"example with spaces" 
Or use  blackslashes between each space. example \ with \ spaces

The filename also starts with --, which makes Linux think it’s an option, so we add -- before it to tell Linux it’s a normal file.

cat -- "--spaces in this filename--"

# Commands Used
ls
cat
--
"" "" 
