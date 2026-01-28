**Basic Linux Commands for Day-to-Day Usage**.

---

### **Introduction to Linux Commands**

- **What are Linux Commands?**
  - Instructions that users can give to the Linux operating system through the command line interface (CLI).
  - Essential for navigating, managing files, and interacting with the system.

---

### **Navigating Directories**

- **pwd (Print Working Directory)**  
  Displays the current directory you're in.

  ```bash
  $ pwd
  ```

  _Example output:_ `/home/user`

- **ls (List)**  
  Lists files and directories in the current directory.

  ```bash
  $ ls
  ```

  _Example output:_ `Documents/  Downloads/  Pictures/`

- **cd (Change Directory)**  
  Changes the current directory.
  ```bash
  $ cd /home/user/Documents
  ```

---

### **Directory Operations**

- **mkdir (Make Directory)**  
  Creates a new directory.

  ```bash
  $ mkdir new_folder
  $ mkdir -p parent/child/grandchild
  ```

- **rmdir (Remove Directory)**  
  Removes an empty directory.
  ```bash
  $ rmdir empty_folder
  ```

---

### **Managing Files**

- **touch**  
  Creates an empty file or updates a file's timestamp.

  ```bash
  $ touch newfile.txt
  ```

- **cp (Copy)**  
  Copies files or directories.

  ```bash
  $ cp file1.txt /home/user/Backup/
  $ cp -r /home/user/Documents/project /home/user/Backup/
  ```

- **mv (Move/Rename)**  
  Moves or renames files or directories.

  ```bash
  $ mv oldname.txt newname.txt
  ```

- **rm (Remove)**  
  Deletes files and folders.
  ```bash
  $ rm file1.txt
  $ rm -rf folder/
  ```

---

### **Viewing File Content**

- **cat**  
  Displays the contents of a file.

  ```bash
  $ cat file.txt
  ```

- **less**  
  View file content one screen at a time.

  ```bash
  $ less largefile.txt
  ```

- **head / tail**  
  Shows the first/last 10 lines of a file.
  ```bash
  $ head file.txt
  $ tail file.txt
  ```

---

### **Editing Files**

- **nano**  
  A simple text editor for editing files in the terminal.

  ```bash
  $ nano file.txt
  ```

---

### **System Monitoring Commands**

- **top**  
  Displays a real-time view of running processes.

  ```bash
  $ top
  ```

- **df (Disk Free)**  
  Shows available disk space on file systems.

  ```bash
  $ df -h
  ```

- **free**  
  Displays available and used memory.
  ```bash
  $ free -h
  ```

---

### **Process Management**

- **ps (Process Status)**  
  Displays information about running processes.

  ```bash
  $ ps aux
  ```

- **kill**  
  Terminates a process by its process ID (PID).

  ```bash
  $ kill 1234
  $ kill -9 1234
  ```

- **killall**  
  Terminates all processes with a given name.
  ```bash
  $ killall firefox
  ```

---

### **Searching & Finding Files**

- **find**  
  Search for files in a directory hierarchy.

  ```bash
  $ find /home/user -name "file.txt"
  ```

- **grep**  
  Searches for a pattern within files.
  ```bash
  $ grep "error" logfile.txt
  $ grep -i "error" logfile.txt          # Case-insensitive search
  $ grep -r "pattern" /path/to/dir       # Recursive search in directory
  $ grep -n "error" logfile.txt          # Show line numbers
  $ grep -v "error" logfile.txt          # Invert match (exclude lines)
  $ grep -c "error" logfile.txt          # Count matching lines
  $ grep -A 3 "error" logfile.txt        # Show 3 lines after match
  $ grep -B 3 "error" logfile.txt        # Show 3 lines before match
  $ grep -C 3 "error" logfile.txt        # Show 3 lines before and after
  $ grep -E "error|warning" logfile.txt  # Extended regex (multiple patterns)
  $ grep -w "word" file.txt              # Match whole words only
  ```

---

### **Text Processing**

- **echo**  
  Prints text to the terminal.

  ```bash
  $ echo "Hello, World!"
  ```

- **wc (Word Count)**  
  Counts lines, words, and characters in a file.

  ```bash
  $ wc file.txt
  $ wc -l file.txt
  ```

- **sort**  
  Sorts lines in a file.

  ```bash
  $ sort file.txt
  ```

- **uniq**  
  Removes duplicate lines from sorted data.
  ```bash
  $ sort file.txt | uniq
  ```

---

### **Basic Networking Commands**

- **ping**  
  Checks the connectivity to another machine.

  ```bash
  $ ping google.com
  ```

- **ifconfig / ip**  
  Displays or configures network interfaces.
  ```bash
  $ ifconfig
  $ ip addr show
  ```

---

### **File Transfer & Download**

- **wget**  
  Downloads files from the internet.

  ```bash
  $ wget https://example.com/file.zip
  ```

- **curl**  
  Transfers data from or to a server.

  ```bash
  $ curl -O https://example.com/file.zip
  ```

- **scp (Secure Copy)**  
  Securely copies files between hosts over SSH.
  ```bash
  $ scp file.txt user@remote:/path/to/destination
  ```

---

### **Remote Access**

- **ssh (Secure Shell)**  
  Connects to a remote machine securely.
  ```bash
  $ ssh user@remote-server.com
  ```

---

### **System Information**

- **whoami**  
  Displays the current username.

  ```bash
  $ whoami
  ```

- **uname**  
  Shows system information.

  ```bash
  $ uname -a
  ```

- **hostname**  
  Displays or sets the system's hostname.

  ```bash
  $ hostname
  ```

- **uptime**  
  Shows how long the system has been running.

  ```bash
  $ uptime
  ```

- **du (Disk Usage)**  
  Shows disk usage of files and directories.
  ```bash
  $ du -sh folder/
  ```

---

### **File Permissions**

- **chmod**  
  Changes file or directory permissions.

  ```bash
  $ chmod 755 script.sh
  ```

- **chown**  
  Changes file ownership.
  ```bash
  $ chown user:user file.txt
  ```

---

### **File Compression & Archives**

- **tar**  
  Creates or extracts archive files.

  ```bash
  $ tar -czf archive.tar.gz folder/
  $ tar -xzf archive.tar.gz
  ```

- **zip / unzip**  
  Compresses or extracts zip files.
  ```bash
  $ zip archive.zip file1.txt file2.txt
  $ unzip archive.zip
  ```

---

### **Command Shortcuts**

- **alias**  
  Creates shortcuts for commands.

  ```bash
  $ alias ll='ls -la'
  $ alias update='sudo apt-get update && sudo apt-get upgrade'
  ```

---

### **Package Management (Ubuntu Example)**

- **apt-get update**  
  Updates the package lists.

  ```bash
  $ sudo apt-get update
  ```

- **apt-get install**  
  Installs a package.
  ```bash
  $ sudo apt-get install vim
  ```

---

## Explore further

1. [More on `ls` and `cp`](file/ls-and-cp.md)
2. [File Permissions](file/permissions.md)
