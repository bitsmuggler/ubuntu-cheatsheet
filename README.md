# Ubuntu Cheatsheet

## Filesystem

| Command  |  Description |
|---|---|
| `lsblk -o NAME,FSTYPE,SIZE,MOUNTPOINT,LABEL`  | It shows: <br> * the name of the drive and the partitions it has <br> * the type of file system <br> * the size the whole drive has and the size each partition has <br> * the mount point and if available, the label for them. |
| `nano /etc/fstab`  |  Edit file which manages mountings to partitions  |
| `mount -a`  |  Mount filesystems (without restart) |
| `df -h`| hows available and used disk space on the Linux system |
| `df -P /srv \| tail -1 \| cut -d' ' -f 1` |  Find out which partition/mount a directory or file is on|
| `resize2fs <<filesystem>>`| Increase the file system to match the logical volume size (if using EXT4)

## Files & Folders

| Command  |  Description |
|---|---|
| `sudo chown $USER /path/to/file`  | Change the user and/or group ownership of a given file, directory, or symbolic link. |
| `cp -R -L -i <<src path>> <<target path>>` | Hardcopy von Files
| `tar -C /myfolder -xvf yourfile.tar`| Extracting a tar in a specific folder
| `tar -xvf yourfile.tar`| Extract tar in the current folder

## Processes

| Command  |  Description |
|---|---|
| `lsof -i:<<Port>>`| Show all processes which are listening on a specific port|
| `kill -9 <<PID>>`  | Kill a process with a specified PID |
| `service --status-all`| List all services |
| `systemctl stop <<your service>>` | Stop a service |

## System

| Command  |  Description |
|---|---|
| `shutdown -r 0`| Reboot ubuntu immediately|


## Let's encrypt (3rd Party)

| Command  |  Description |
|---|---|
| `certbot certonly --standalone --preferred-challenges http -d <<domain>>`| Create certificate |

