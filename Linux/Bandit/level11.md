# Level 11 → 12

# Task
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Solution
The file was encoded with ROT13, which shifts each letter 13 places in the alphabet. I used  cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' to decode the text, which revealed the password.

## Key Commands 
- tr
- cat
