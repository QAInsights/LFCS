# LFCS Tips

## Exam tips

- Login into the right machine before attempting to answer the questions
- Read the questions atleast twice
- Understand the copy and paste shortcut between the question pane and the virtual machine as it varies due to OS
- Use `apropos`, `man` and `info` command to get some initial help
- If no help found, use `find` by searching for a keyword (time consuming)
- If no help found, use `locate` by searching for a keyword (less time consuming); you may to install it first and use `updatedb` to update the database
- Look out for typo while naming, configuring, permission string etc.
- Use `fg` and `bg` efficiently
- Use `ps` and `jobs` to keep track of the running processes
- Use `htop` instead of `top`
- Always mark your questions for review
- Always manually navigate to each question using the `prev` and `next` buttons
- Switch to `sudo` whenever is necessary
- Whenever you create a file, make sure the content is properly formatted and the proper permissions have been configured
- Use `git` log to validate the git commit
- Use `git diff` to validate the git commit
- Use `docker` commands to validate the container/image/logs

## Sample questions

- Build and install software from source
- Fix `apache` process to start successfully
- Find the large files recursively and delete the largest one
- Find the files based on the permissions
- Find the high CPU and high read process and kill it
- Git init, commit, and push it to remote
- Docker run command with restart policy, port, and image
- Extend LV 
- Create a swap partition and add it to `/etc/fstab`
- Mount NFS with `ro`, `rw` w/ `security` options
- Create a netfilter to allow port 8080
- Enable ntp and change the timezone
- Change `nproc` for the user `hard` and `soft` limit
- Schedule a cron tab for the user to take a backup
- Configure sshd to allow keyboard authentication for the user
- Create a bash script and run it as a cron job
- Creae a new user and add it to the group e.g. `sudo` 
    - Make the group as primary/secondary
- Create vm swappiness and set it to `10`; make it persistent
- Create a xfs filesystem and mount it
- Create a VM using `virt-install` and autostart it
- Fix the high disk usage by deleting the files and by finding the mount
- Find the correct certificate and private key and delete the others
- Generate the certificate for the new CN 


## Useful commands

### General Linux commands

- `man`
- `info`
- `locate`
- `find`
- `updatedb`
- `htop`
- `top`
- `ps`
- `jobs`
- `fg`
- `bg`
- `sudo`

### find commands

- `find / -name "file_name" -type f`
- `find / -name "file_name" -type d`
- `find / -name "file_name" -type l`
- `find / -name "file_name" -type s`
- `find / -name "file_name" -user "username"`
- `find / -name "file_name" -group "groupname"`
- `find / -name "file_name" -perm 777`

### git commands

- `git init`
- `git add`
- `git commit`
- `git push`
- `git log`
- `git diff`
- `git status`

### docker commands

- `docker run`
- `docker ps`
- `docker logs`
- `docker start`
- `docker stop`
- `docker restart`
- `docker rm`
- `docker rmi`
- `docker pull`
- `docker exec`
- `docker image`

### crontab commands

- `crontab -l`
- `crontab -e`
- `crontab -u username -l`
- `crontab -u username -e`

### iptables commands

- `iptables -L`
- `iptables -A INPUT -i eth0 -p tcp --dport 80 -j ACCEPT`
- `iptables -D INPUT -i eth0 -p tcp --dport 80 -j ACCEPT`

### ufw commands

- `ufw status`
- `ufw allow 80/tcp`
- `ufw deny 80/tcp`
- `ufw delete allow 80/tcp`
- `ufw delete deny 80/tcp`

### ntp commands

- `timedatectl status`
- `timedatectl set-timezone "Asia/Kolkata"`
- `timedatectl set-ntp true`
- `timedatectl set-ntp false`

### sysctl commands

- `sysctl -a`
- `sysctl -p /etc/sysctl.conf`

### nproc commands

- `ulimit -a`
- `ulimit -n 1000`
- `ulimit -u 1000`
- `ulimit -S 1000`
- `ulimit -H 1000`

### systemctl commands

- `systemctl status`
- `systemctl start`
- `systemctl stop`
- `systemctl restart`
- `systemctl enable`
- `systemctl disable`
- `systemctl list-unit-files`
- `systemctl list-units`

### sshd commands

- `sshd -t`
- `sshd -t -f /etc/ssh/sshd_config`

### vim commands

- `:w`
- `:q`
- `:q!`
- `:wq`
- `:wq!`

### xfs commands

- `mkfs.xfs`
- `mount`
- `umount`

### mkswap commands

- `swapon`
- `swapoff`

### lv, pv, vg commands

- `lvcreate`
- `lvremove`
- `vgcreate`
- `vgremove`
- `pvcreate`
- `pvremove`

### virt-install commands

- `virt-install`
- `virsh list`
- `virsh start`
- `virsh stop`
- `virsh destroy`
- `virsh console`
- `virsh attach-device`

## Conclusion

Here's a summary of my experience with the LFCS exam and additional tips that might help you succeed:

1. Time Management
   - The exam is time-sensitive, so practice completing tasks quickly
   - Skip complex questions initially and return to them later
   - Allocate more time for complex tasks like storage management and container operations
   - Keep track of time - aim to spend no more than 5-7 minutes per question

2. System Navigation
   - Master keyboard shortcuts for faster navigation
   - Keep multiple terminal windows open for different tasks
   - Use tmux or screen for better terminal management
   - Create a quick reference of commonly used paths (/etc/, /var/log/, etc.)

3. Command Line Efficiency
   - Use tab completion extensively
   - Master command history (Ctrl+R for search)
   - Utilize command line aliases for frequent operations
   - Keep command syntax simple and verify before execution

4. Problem-Solving Approach
   - Always verify your work after completing a task
   - If a command fails, check logs immediately (/var/log/)
   - Have multiple approaches ready for each type of task
   - Don't hesitate to use built-in help (man, info, --help)

5. Critical Areas to Focus
   - Storage management (LVM, file systems)
   - Service management with systemd
   - Network configuration and troubleshooting
   - Container operations (especially Docker)
   - User and permission management

Remember: The exam environment is designed to test real-world scenarios. Practice in a non-GUI environment, and focus on understanding the concepts rather than memorizing commands. Good luck!
