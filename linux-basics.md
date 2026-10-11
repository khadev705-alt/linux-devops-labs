
# Linux Commands Cheat Sheet for Cloud & DevOps Engineers

A practical reference guide to essential Linux commands for beginners preparing for Cloud Computing, DevOps Engineering, System Administration, and Infrastructure Automation.

## Table of Contents

1. Navigation Commands
2. File and Directory Management
3. File Content Commands
4. Search Commands
5. System Information
6. Users and Permissions
7. Process Management
8. Networking Commands
9. Package Management
10. Archive and Compression
11. Bash Scripting
12. Logs and Services
13. Disk and Memory Management
14. Environment Variables
15. SSH Commands
16. Git and GitHub Commands
17. Input and Output Redirection
18. Useful Keyboard Shortcuts

---

## 1. Navigation Commands

| Command | Description |
|---|---|
| `pwd` | Display the current working directory |
| `ls` | List files and directories |
| `ls -l` | Display detailed file information |
| `ls -a` | Show hidden files and directories |
| `ls -lh` | Display file sizes in human-readable format |
| `ls -lt` | Sort files by modification time |
| `cd /path` | Change to a specific directory |
| `cd ..` | Move to the parent directory |
| `cd ~` | Move to the home directory |
| `cd -` | Return to the previous directory |
| `tree` | Display directory structure as a tree |
| `clear` | Clear the terminal screen |
| `history` | Display previously executed commands |

## 2. File and Directory Management

| Command | Description |
|---|---|
| `touch file.txt` | Create an empty file |
| `mkdir folder` | Create a directory |
| `mkdir -p a/b/c` | Create nested directories |
| `cp file.txt backup.txt` | Copy a file |
| `cp -r source/ destination/` | Copy a directory recursively |
| `mv old.txt new.txt` | Rename a file |
| `mv file.txt folder/` | Move a file to another directory |
| `rm file.txt` | Delete a file |
| `rmdir folder` | Remove an empty directory |
| `rm -r folder/` | Remove a directory and its contents |
| `file file.txt` | Identify the file type |
| `stat file.txt` | Display file metadata |
| `basename /home/user/file.txt` | Display the filename |
| `dirname /home/user/file.txt` | Display the parent directory path |
| `ln -s target link` | Create a symbolic link |

**Warning:** Deletion commands can permanently remove data. Verify paths before using `rm -r` or `rm -rf`.

## 3. File Content Commands

| Command | Description |
|---|---|
| `cat file.txt` | Display file contents |
| `less file.txt` | Read a file page by page |
| `more file.txt` | Display file contents page by page |
| `head file.txt` | Display the first 10 lines |
| `head -n 20 file.txt` | Display the first 20 lines |
| `tail file.txt` | Display the last 10 lines |
| `tail -n 50 file.txt` | Display the last 50 lines |
| `tail -f app.log` | Follow new log entries in real time |
| `nano file.txt` | Open a file in the Nano editor |
| `wc file.txt` | Count lines, words, and bytes |
| `wc -l file.txt` | Count lines |
| `sort file.txt` | Sort lines alphabetically |
| `uniq file.txt` | Remove adjacent duplicate lines |
| `diff file1.txt file2.txt` | Compare two files |
| `tee output.txt` | Display output and write it to a file |

## 4. Search Commands

| Command | Description |
|---|---|
| `find . -name "*.log"` | Find files with a specific extension |
| `find . -type f` | Find regular files |
| `find . -type d` | Find directories |
| `find . -iname "readme*"` | Find files case-insensitively |
| `grep "error" app.log` | Search for a word in a file |
| `grep -i "error" app.log` | Search without case sensitivity |
| `grep -n "error" app.log` | Display matching line numbers |
| `grep -r "TODO" .` | Search recursively in a directory |
| `grep -v "INFO" app.log` | Display lines that do not match |
| `grep -E "error|fail" app.log` | Search using extended patterns |
| `which python3` | Display the executable path |
| `command -v git` | Check whether a command is available |
| `locate file.txt` | Search using the locate database |

## 5. System Information

| Command | Description |
|---|---|
| `whoami` | Display the current username |
| `id` | Display user and group IDs |
| `uname -a` | Display kernel and system information |
| `hostname` | Display the system hostname |
| `hostnamectl` | Display hostname and OS information |
| `date` | Display the current date and time |
| `uptime` | Display system uptime and load averages |
| `free -h` | Display memory usage |
| `df -h` | Display filesystem disk usage |
| `du -sh folder/` | Display the total size of a directory |
| `lsblk` | List block storage devices |
| `lscpu` | Display CPU information |
| `cat /etc/os-release` | Display Linux distribution information |
| `printenv` | Display environment variables |
| `dmesg` | Display kernel messages |
| `timedatectl` | Display system time and timezone information |

## 6. Users and Permissions

| Command | Description |
|---|---|
| `who` | Display logged-in users |
| `w` | Display logged-in users and their activity |
| `groups` | Display the current user's groups |
| `sudo command` | Execute a command with elevated privileges |
| `chmod 755 script.sh` | Set file permissions |
| `chmod +x script.sh` | Make a file executable |
| `chmod 644 file.txt` | Set owner read/write and others read permissions |
| `chown user file.txt` | Change file ownership |
| `chown user:group file.txt` | Change owner and group |
| `chgrp group file.txt` | Change the file group |
| `umask` | Display the default permission mask |
| `passwd` | Change a user's password |
| `sudo useradd username` | Create a user account |
| `sudo userdel username` | Delete a user account |
| `sudo usermod -aG group username` | Add a user to a supplementary group |

Permission symbols:

- `r` = Read
- `w` = Write
- `x` = Execute

Example: `chmod 755 script.sh` gives the owner read/write/execute permissions and gives group and others read/execute permissions.

## 7. Process Management

| Command | Description |
|---|---|
| `ps` | Display processes associated with the current shell |
| `ps aux` | Display running processes |
| `top` | Monitor processes and resource usage |
| `htop` | Interactive process monitoring; may require installation |
| `pgrep nginx` | Find process IDs by name |
| `kill PID` | Send the default termination signal |
| `kill -15 PID` | Request graceful process termination |
| `kill -9 PID` | Forcefully terminate a process |
| `pkill process_name` | Send a signal to processes by name |
| `jobs` | List jobs in the current shell |
| `bg` | Resume a suspended job in the background |
| `fg` | Bring a shell job to the foreground |
| `nohup command &` | Run a command that can survive terminal disconnection |
| `nice -n 10 command` | Start a process with a specified scheduling priority |
| `renice` | Change the priority of a running process |

## 8. Networking Commands

| Command | Description |
|---|---|
| `ip addr` | Display network interface addresses |
| `ip link` | Display network interfaces |
| `ip route` | Display routing information |
| `ping example.com` | Test network reachability |
| `curl https://example.com` | Send an HTTP request |
| `curl -I https://example.com` | Display HTTP response headers |
| `wget URL` | Download a file from a URL |
| `ss -tuln` | Display listening TCP and UDP ports |
| `ss -tpn` | Display TCP connections and available process details |
| `dig example.com` | Query DNS records |
| `nslookup example.com` | Perform a DNS lookup |
| `traceroute example.com` | Trace a network route; may require installation |
| `ssh user@host` | Connect to a remote system securely |
| `scp file.txt user@host:/path/` | Copy a file over SSH |
| `rsync -av source/ destination/` | Synchronize files and directories |
| `hostname -I` | Display available local IP addresses |

## 9. Package Management (Ubuntu)

| Command | Description |
|---|---|
| `sudo apt update` | Refresh package lists |
| `sudo apt upgrade` | Upgrade installed packages |
| `sudo apt install nginx` | Install a package |
| `sudo apt remove nginx` | Remove a package |
| `sudo apt purge nginx` | Remove a package and its system configuration |
| `apt search nginx` | Search for packages |
| `apt show nginx` | Display package information |
| `dpkg -l` | List installed packages |
| `sudo apt autoremove` | Remove automatically installed, unused dependencies |
| `sudo apt clean` | Clear the downloaded package cache |
| `dpkg -L package_name` | List files installed by a package |

## 10. Archive and Compression

| Command | Description |
|---|---|
| `tar -cvf archive.tar folder/` | Create a TAR archive |
| `tar -xvf archive.tar` | Extract a TAR archive |
| `tar -czvf archive.tar.gz folder/` | Create a compressed TAR archive |
| `tar -xzvf archive.tar.gz` | Extract a compressed TAR archive |
| `gzip file.txt` | Compress a file |
| `gunzip file.txt.gz` | Decompress a Gzip file |
| `zip -r archive.zip folder/` | Create a ZIP archive; may require installation |
| `unzip archive.zip` | Extract a ZIP archive |

## 11. Bash Scripting

| Command or Syntax | Description |
|---|---|
| `echo "Hello"` | Print text |
| `read name` | Read user input |
| `#!/bin/bash` | Specify the Bash interpreter |
| `bash script.sh` | Execute a Bash script |
| `./script.sh` | Execute a script with executable permission |
| `chmod +x script.sh` | Make a script executable |
| `export NAME=value` | Export an environment variable |
| `source ~/.bashrc` | Reload Bash configuration in the current shell |
| `sleep 5` | Pause for five seconds |
| `exit 0` | Exit successfully |
| `date +%F` | Display the date in YYYY-MM-DD format |
| `$(command)` | Substitute command output |
| `command1 && command2` | Run the second command if the first succeeds |
| `command1 || command2` | Run the second command if the first fails |
| `command1 \| command2` | Pass output to another command |
| `if [ condition ]; then ...; fi` | Execute commands conditionally |
| `for item in list; do ...; done` | Repeat commands for each item |
| `while [ condition ]; do ...; done` | Repeat commands while a condition holds |
| `$1`, `$2` | Access positional script arguments |
| `$?` | Read the previous command's exit status |
| `$#` | Get the number of positional arguments |
| `"$@"` | Access all positional arguments safely |

## 12. Logs and Services

| Command | Description |
|---|---|
| `journalctl` | Display systemd journal logs |
| `journalctl -u nginx` | Display logs for a specific service |
| `journalctl -f` | Follow new journal entries |
| `journalctl -p err` | Display error-priority messages |
| `systemctl status nginx` | Display service status |
| `sudo systemctl start nginx` | Start a service |
| `sudo systemctl stop nginx` | Stop a service |
| `sudo systemctl restart nginx` | Restart a service |
| `sudo systemctl reload nginx` | Request a service configuration reload |
| `sudo systemctl enable nginx` | Enable a service at boot |
| `sudo systemctl disable nginx` | Disable automatic startup |
| `logger "Test message"` | Write a message to the system log |

Note: Service-management commands require systemd and appropriate permissions. Their availability may vary in WSL.

## 13. Disk and Memory Management

| Command | Description |
|---|---|
| `df -h` | Display filesystem space usage |
| `df -i` | Display inode usage |
| `du -sh *` | Display sizes of items in the current directory |
| `du -h --max-depth=1 /var` | Display top-level directory sizes |
| `free -h` | Display RAM and swap usage |
| `vmstat 1 5` | Display system statistics at one-second intervals |
| `lsblk -f` | Display block devices and filesystem information |
| `findmnt` | Display mounted filesystems |
| `sync` | Request that buffered filesystem data be written |
| `ulimit -a` | Display shell resource limits |

## 14. Environment Variables

| Command | Description |
|---|---|
| `env` | Display environment variables |
| `printenv HOME` | Display the HOME variable |
| `echo $PATH` | Display the executable search path |
| `export APP_ENV=dev` | Export an environment variable |
| `unset APP_ENV` | Remove a shell variable |
| `env VAR=value command` | Run a command with a temporary environment variable |
| `source ~/.bashrc` | Load Bash configuration into the current shell |
| `set` | Display shell variables and functions |
| `which python3` | Display the executable path when available |

Avoid putting passwords, access tokens, or other secrets directly into shell history or public repository files.

## 15. SSH Commands

| Command | Description |
|---|---|
| `ssh user@host` | Connect to a remote host |
| `ssh -T git@github.com` | Test GitHub SSH authentication |
| `ssh-keygen -t ed25519 -C "email@example.com"` | Generate an SSH key pair |
| `cat ~/.ssh/id_ed25519.pub` | Display the public key |
| `ssh-add ~/.ssh/id_ed25519` | Add a private key to the SSH agent |
| `ssh-keygen -lf ~/.ssh/id_ed25519.pub` | Display a public key fingerprint |
| `ssh -v user@host` | Connect with verbose troubleshooting output |
| `scp file.txt user@host:/path/` | Copy a file to a remote host |

Never publish or share your private SSH key. Only the `.pub` public key should be added to GitHub.

## 16. Git and GitHub Commands

| Command | Description |
|---|---|
| `git --version` | Display Git version |
| `git config --global --list` | Display global Git configuration |
| `git status` | Display working tree status |
| `git clone URL` | Clone a repository |
| `git add file.txt` | Stage a file |
| `git add .` | Stage changes under the current directory |
| `git commit -m "message"` | Create a commit |
| `git push` | Push commits to a remote repository |
| `git pull` | Fetch and integrate remote changes |
| `git fetch` | Fetch remote references and objects |
| `git log --oneline` | Display concise commit history |
| `git diff` | Display unstaged changes |
| `git diff --staged` | Display staged changes |
| `git branch` | List local branches |
| `git switch -c feature` | Create and switch to a branch |
| `git merge feature` | Merge a branch |
| `git remote -v` | Display remote repository URLs |
| `git restore file.txt` | Discard unstaged changes to a tracked file |
| `git rm file.txt` | Stage deletion of a tracked file |
| `git stash` | Temporarily save tracked working changes |
| `git show` | Display details of a commit or Git object |

## 17. Input and Output Redirection

| Syntax | Description |
|---|---|
| `command > output.txt` | Write standard output, replacing the file |
| `command >> output.txt` | Append standard output |
| `command < input.txt` | Read standard input from a file |
| `command 2> error.log` | Redirect standard error |
| `command > output.txt 2>&1` | Redirect standard output and standard error to the same destination |
| `command1 \| command2` | Pipe standard output to another command |
| `command1 \| tee output.txt` | Display output and save it to a file |
| `sort file.txt \| uniq` | Sort lines and remove adjacent duplicates |
| `grep "error" app.log \| wc -l` | Count matching error lines |

## 18. Useful Keyboard Shortcuts

| Shortcut | Description |
|---|---|
| `Ctrl + C` | Interrupt the foreground command |
| `Ctrl + D` | Send end-of-input to the terminal |
| `Ctrl + L` | Clear the terminal display |
| `Ctrl + A` | Move to the beginning of the command line |
| `Ctrl + E` | Move to the end of the command line |
| `Ctrl + U` | Delete from the cursor to the beginning of the line |
| `Ctrl + K` | Delete from the cursor to the end of the line |
| `Ctrl + R` | Search command history |
| `Tab` | Complete commands, filenames, and paths |
| `Up Arrow` | Recall the previous command |
| `Down Arrow` | Navigate forward through command history |

---

## Recommended Learning Order for Cloud & DevOps

1. Linux navigation and file management
2. File permissions and user administration
3. Processes, services, logs, and troubleshooting
4. Networking fundamentals and SSH
5. Bash scripting and automation
6. Git and GitHub
7. Cloud virtual machines and server administration
8. Docker and container management
9. CI/CD pipelines
10. Infrastructure as Code with Terraform
11. Configuration management and monitoring

## Practice Guidelines

- Practice commands in your Ubuntu WSL environment.
- Use test directories when learning file deletion and permission commands.
- Understand the output of each command rather than memorizing syntax alone.
- Document practical exercises in this repository.
- Never commit private keys, credentials, passwords, or production secrets.

**Goal:** Build practical Linux administration and automation skills that form the foundation of a Cloud & DevOps Engineering career.
