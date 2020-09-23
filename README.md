# Ubuntu Cheatsheet

## Files & Folders

| Command  |  Description |
|---|---|
| `sudo chown $USER /path/to/file`  | Change the user and/or group ownership of a given file, directory, or symbolic link. |
| `nano /etc/fstab`  |  Edit file which manages mountings to partitions  |
| `mount -a`  |  Mount filesystems (without restart) |
| `df -P /srv \| tail -1 \| cut -d' ' -f 1` |  Find out which partition/mount a directory or file is on|
| `cp -R -L -i <<src path>> <<target path>>` | Hardcopy von Files

## Processes

| Command  |  Description |
|---|---|
| `lsof -i:<<Port>>`| Show all processes which are listening on a specific port|
| `kill -9 <<PID>>`  | Kill a process with a specified PID |
| `service --status-all`| List all services |
| `systemctl start <<your service>>` | Stop a service |

## Let's encrypt (3rd Party)

| Command  |  Description |
|---|---|
| `certbot certonly --standalone --preferred-challenges http -d <<domain>>`| Create certificate |

