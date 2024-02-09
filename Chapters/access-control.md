# Access Control
Linux uses a system of users and groups to handle access control. Each user has a unique UID and an associated user name. Users can be added to groups, which have a unique GID.

Files and directories have permissions metadata that controls which users and groups can interact with them.

## File and directory permissions

Linux has three file permissions; read write and execute.

### Read (r)

The read permission (denoted as ```r```) allows a user to view and read the contents of a file. It also allows limited access to list the contents of a directory.

### Write (w)

The write permission (denoted as ```w```) grants the ability to modify the contents of a file or add, remove, and rename files within a directory.

### Execute (x)

The execute permission (denoted as ```x```), for files, allows a user to run the file as a program or script. It also allows a user to access a directory.

### View permissions of all files in current directory
```
$ ls -la
```
Example output
```
$ ls -la
drwxr-x---  14 myuser myuser 4.0K Mar  8  2022 .
drwxr-xr-x  19 root   root   4.0K Mar  7  2022 ..
drwxrwx---  4  myuser myuser 4.0K Dec  8 08:01 .config
drwx------  2  myuser myuser 4.0K Dec  3 09:31 .ssh
-rw-r-----  1  myuser mygroup 91K Nov 25 14:05 picture.jpg
-rw-rw----  1  myuser myuser 102M Oct 22 09:42 video.mkv
```
Permissions are reported by the ls command as a 10 character string. In the above example, the permissions for the file **picture.jpg** are ```-rw-rw-r--```.

|Type   | Owner permissions (u) | Group permissions (g) | Others permissions (o)|
|-------|-------------------|-------------------|--------------------|
|```-```| ```rw-```         | ```r--```         | ```---```          |

### File type
The type character signifies the type of file that this is. Regular files are designated with a ```-```, directories are designated with a ```d```.

### Owner permissions (u)
These three characters indicate the permissions that the user that owns the file has.

### Group permissions (g)
These three characters indicate the permissions that the group that owns the file has. These permissions apply to all users that are members of the group that owns the file.

### Others permissions (o)
These three characters indicate the permissions that users and groups who are not the file owner and not a member of the group that owns the file.

## Changing ownership and permissions

It is often neccesary to change the owner or permissions of a file or directory.

Standard users cannot change the owner of a file, but they can change the group to any group that they are a member of. 

### Change owner
The ```chown``` command (**CH**ange **OWN**er) chages the user, and optionally the group, that owns a file.

```# chown [<OPTIONS>] <username>[:<group>] /path/to/file```

#### Change owner of single file
```# chown devuser ~/Downloads/Picture.gif```

Changes the owner of ```~/Downloads/Picture.gif``` to the user "devuser".

#### Change owner and group of single file
```# chown devuser:developers /mnt/share/Picture.gif```

Changes the owner of ```/mnt/share/Picture.gif``` to the user "devuser" and the group "developers".

### Change group
The ```chgrp``` command (**CH**ange **OWN**er) chages the user, and optionally the group, that owns a file.

