# Ubuntu Cheatsheet

## Filesystem

| Command  |  Description |
|---|---|
| `lsblk -o NAME,FSTYPE,SIZE,MOUNTPOINT,LABEL`  | It shows: <br> * the name of the drive and the partitions it has <br> * the type of file system <br> * the size the whole drive has and the size each partition has <br> * the mount point and if available, the label for them. |
| `nano /etc/fstab`  |  Edit file which manages mountings to partitions  |
| `mount -a`  |  Mount filesystems (without restart) |
| `df -h`| hows available and used disk space on the Linux system |
| `df -P /srv \| tail -1 \| cut -d' ' -f 1` |  Find out which partition/mount a directory or file is on|
| `resize2fs [filesystem]`| Increase the file system to match the logical volume size (if using EXT4)

## Files & Folders

| Command  |  Description |
|---|---|
| `sudo chown $USER /path/to/file`  | Change the user and/or group ownership of a given file, directory, or symbolic link. |
| `cp -R -L -i [src path] [target path]` | Hardcopy von Files
| `tar -C /myfolder -xvf yourfile.tar`| Extracting a tar in a specific folder
| `tar -xvf yourfile.tar`| Extract tar in the current folder
| `chmod -R 777 [folder]`| Change folder & file permissions to full
| `ll or ls -l`| Get detail information about files and directories in present working directory


## Processes

| Command  |  Description |
|---|---|
| `lsof -i:[Port]`| Show all processes which are listening on a specific port|
| `kill -9 [PID]`  | Kill a process with a specified PID |
| `service --status-all`| List all services |
| `systemctl stop [your service]` | Stop a service |
| `systemctl disable [your service]`| Disable a service |
| `[your command] &` | Running a command as background job |
| `jobs` | List background jobs |
| `kill [number]` | Kill specific background job`
| `ps \| grep <<your command or process name>>` | Find a specific running process |

## Packagemanagement

| Command  |  Description |
|---|---|
| `apt-get remove [package-name]`| Remove a specific package|


## System

| Command  |  Description |
|---|---|
| `shutdown -r 0`| Reboot ubuntu immediately|
| `history` | Show the commands history in the shell
|`getent passwd´| Get list of all users

## Let's encrypt (3rd Party)

| Command  |  Description |
|---|---|
| `certbot certonly --standalone --preferred-challenges http -d [domain]`| Create certificate |

## Shortcuts

| Shortcut  |  Description |
|---|---|
| `CTRL + R`| Will start search from most recent command to old one |


