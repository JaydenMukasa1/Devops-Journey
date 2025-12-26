Level 8 → 9

Task
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Solution
Sort to organise the file so duplicate lines are grouped together, then used uniq -u to show only the line that appears once. Ran `sort data.txt | uniq -u` and it returned the password.


Key Commands 
sort
uniq

