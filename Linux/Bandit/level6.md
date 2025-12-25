Level 6 → 7

Task
Find the password for the next level somewhere on the server. The file is owned by user bandit7, group bandit6, and is exactly 33 bytes in size.

Solutions 
Used find to search for the file by its properties: user bandit7, group bandit6, and size 33 bytes. Ran find / -user bandit7 -group bandit6 -size 33c 2>/dev/null, it returned the correct file path, then used cat to read the password.

Key commands
find 
cat 
2>/dev/null
