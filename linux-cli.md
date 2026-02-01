# Linux CLI Cheat Sheet

*Built for operators. Maintained in the open.*

Essential Linux command-line commands for navigating systems, inspecting files,
and performing safe day-to-day operations in servers, containers, and bastion hosts.

---

## Where Am I?

pwd                 → print working directory

whoami              → current user

hostname            → system hostname

uname -a            → kernel and system info

---


## Directory Navigation

i                   → insert mode (start editing)

ls                  → list files

ls -la              → detailed list (including hidden files)

cd /path            → change directory

cd ..               → up one directory

cd ~                → home directory

cd /                → filesystem root

---


## Files & Directories

touch file.txt       → create empty file

mkdir dir            → create directory

rmdir dir            → remove empty directory

cp src dst           → copy file

cp -r dir1 dir2      → copy directory recursively

mv src dst           → move or rename

rm file              → delete file

rm -rf dir           → delete directory recursively (DANGEROUS)

---


## Viewing Files

cat file.txt        → print file contents

less file.txt       → paged view (q to quit)

head file.txt       → first 10 lines

tail file.txt       → last 10 lines

tail -f file.txt    → follow file output (logs)

---


## Searching & Filtering

grep text file      → search for text in file

grep -R text dir    → recursive search

|                   → pipe output to another command


# Example:
ps aux | grep nginx

---


## Processes

ps aux              → list running processes

top                 → live process view

htop                → enhanced process view (if installed)

kill PID            → terminate process

kill -9 PID         → force kill (last resort)

---


## Disk & Memory

df -h               → disk usage by filesystem

du -sh dir          → size of directory

free -h             → memory usage

---


## Networking

ip a                → network interfaces

ss -lntp            → listening ports

curl url            → HTTP request

ping host           → connectivity test

---


## Permissions & Ownership

ip a                  → network interfaces

ls -l                 → view permissions

chmod 644 file        → change file permissions

chmod +x script.sh    → make executable

chown user:group file → change ownership

---


## Environment & Shell

env                 → list environment variables

echo $VAR           → print variable

export VAR=value    → set variable (current shell)

history             → command history

clear               → clear screen

---


## Operator Safety Tips

 - Pause before running rm -rf
   
 - Verify your path with pwd
   
 - Use less instead of cat for large files
   
 - Read commands twice before pressing Enter
