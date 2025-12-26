Level 9 → 10

Task
Password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

Solution
Used grep to search the file for the pattern ===. First I viewed the file with cat to see the contents, then ran `grep "===" data.txt` to find the line containing it, which showed the password.

Key Commands 
grep
cat
