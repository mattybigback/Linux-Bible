# Access Control
Linux uses a system of users and groups to handle access control. Each user has a unique UID and an associated user name. Users can be added to groups, which have a unique GID.

Files and directories have permissions metadata that controls which users and groups can interact with them.

## File and directory permissions
##View permissions of all files in current directory
```
$ ls -la
```
Example output
```
$ ls -la
drwxr-x---  14 myusername myusername 4.0K Mar  8  2022 .
drwxr-xr-x  19 root       root       4.0K Mar  7  2022 ..
drwxrwx---  4  myusername myusername 4.0K Dec  8 08:01 .config
drwx------  2  myusername myusername 4.0K Dec  3 09:31 .ssh
-rw-r-----  1  myusername mygroup     91K Nov 25 14:05 picture.jpg
-rw-rw----  1  myusername myusername 102M Oct 22 09:42 video.mkv
```
Permissions are reported by the ls command as a 10 character string. In the above example, the permissions for the file **picture.jpg** are ```-rw-rw-r--```.

|Type   | Owner permissions | Group permissions | Global permissions |
|-------|-------------------|-------------------|--------------------|
|```-```| ```rw-```         | ```r--```         | ```---```          |

### File type
The type character signifies the type of file that this is. Regular files are designated with a ```-```.

### Owner permissions
The three characters indicate the permissions that the owner of the file has.