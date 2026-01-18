## Challenge 3: File operations script 

Create a script that checks if a file exists and displays its permissions.

---

### Requirements
Prompt user for a filename
Check if the file exists
If it exists, check if it's readable, writable, and executable
Display appropriate messages for each permission
Example output:

Enter filename to check: /etc/passwd
File '/etc/passwd' exists. ✓ File is readable ✓ File is writable ✗ File is not executable

---

### Solution
```bash

echo "Please enter filename"
read filename 
result=$filename

if test -f $filename; then
    echo "File $filename exists";
    else
        echo "File $filename doesn't exist."
fi

readable=

if [ -r $filename ]; then
    readable="is readable"
    else
    readable="is not readable"
fi

writable=
if [ -w $filename ]; then
    writable="is writable"
    else
    writable="is not writable"
fi

executable=
if [ -w $filename ]; then
    executable="is executable"
    else
    executable="is not executable"
fi

echo "$filename $readable. $filename $writable. $filename $executable"
