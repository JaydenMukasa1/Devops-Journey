## Challenge 2: File operations script 

Create a script that automates directory and file creation.

---

### Requirements

- Create a directory called bash_demo
- Navigate into the directory
- Create a file called demo.txt
- Write text to the file (include current date)
- Display the file contents

---


### Solution

```bash
mkdir bash_demo
cd bash_demo
touch demo.txt
echo "This file was created by a Bash script on $(date)" >> demo.txt
cat demo.txt
