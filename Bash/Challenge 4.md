## Challenge 4: Backup Script for Text Files 

Create a script that backs up all .txt files from one directory to another.

---

### Requirements
- Prompt user for source directory
- Create a backup directory if it doesn't exist
- Copy all .txt files to the backup directory
- Add timestamp to backup directory name
- Display count of files backed up

Example output:

Enter source directory: /home/user/documents

Backup directory created: backup_2024-11-29_14-30 Copying .txt files...

Backup complete! Files backed up: 5

---

### Solution
```bash
echo "Enter source directory: "
read directory_name

backup_dir="backup_$(date '+%d-%m-%y')"
mkdir "$backup_dir"
echo "Backup directory created: $backup_dir"
echo "Copying all .txt files..."

cp "$directory_name"/*.txt "$backup_dir"/ 2>/dev/null

count=$(ls "$backup_dir"/*.txt 2>/dev/null | wc -l)

echo "$count files backed up to $backup_dir"
