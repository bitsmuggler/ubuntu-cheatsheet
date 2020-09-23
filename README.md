# Ubuntu Cheatsheet

## Files & Folders

| Command  |  Description |
|---|---|
| `sudo chown $USER /path/to/file`  | Change the user and/or group ownership of a given file, directory, or symbolic link. |
| `nano /etc/fstab`  |  Edit mountings to partitions  |
| `mount -a`  |  Mount filesystems (without restart) |
| `df -P /srv | tail -1 | cut -d' ' -f 1`|  Find out which partition/mount a directory or file is on|

