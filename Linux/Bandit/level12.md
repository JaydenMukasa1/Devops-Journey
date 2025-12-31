Level 12 → 13

Task
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Solution
I started by checking what type of file I was dealing with using file. It was a hexdump, so I reversed it back into a normal binary file with xxd -r. Then I kept using file after each step to see what format it was and used the correct decompression/decoding commands each time (like gzip, bzip2, tar, or base64). By repeating this process, I eventually removed all layers and got the final password.

Key Commands 
file <filename>
xxd -r 
gunzip / gzip -d
bunzip2 / bzip2 -d
tar xf
base64 -d
cp 
mktemp -d
