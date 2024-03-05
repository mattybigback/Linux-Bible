# File Management

## Create, Read, Update, Delete

### Create a new empty file

It is sometimes neccesary to create an empty file. This can be done using the ```touch``` command.

```$ touch /path/to/file```

Using ```touch``` on a file that already exists will not modify the file, but it will update the accessed and modified timestamps.

To create a text file that you intend to modify straight away, such as a new config file, you can type the command for your favourite editor followed by the path to the file. This will open the editor in a state where saving or writing out the file will save to the path you specify.

``` $ vim /path/to/file```

``` $ nano /path/to/file```

### View the contents of a file

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