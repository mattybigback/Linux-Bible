# File Management

## Create, Read, Update, Delete

### Create a new empty file

Touch

### See the contents of a file

There are many ways to view the contents of text files from the command line. Two of the most commonly used commands are ```cat``` and ```less```

For smaller files (no more than a few lines), use the ```cat``` command.

```$ cat /path/to/file```

For larger files, the ```less``` command is more useful, as it allows for scrolling using the cursor keys, as well as `Home`, `End`, `PgUp`, and `PgDn`.

```$ less /path/to/file```

To quit, press `q`.

### Append to the end of a file

\>>

### Replace contents of a file

\>

### Move files or directories

mv

```$ mv [<OPTIONS>] /path/to/source /path/to/destination```

### Rename a file or directory

There is no dedicated command for renaming files in Linux. Instead the file is moved from one file name to another.

```$ mv [<OPTIONS>] oldname newname```

### Delete a file

rm

### Delete a directory and all of its contents

rm -rf