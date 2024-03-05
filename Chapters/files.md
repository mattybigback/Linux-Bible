# File Management

## Create, Read, Update, Delete

### Create a new empty file

It is sometimes neccesary to create an empty file. This can be done using the `touch` command.

```$ touch /path/to/file```

Using ```touch``` on a file that already exists will not modify the file, but it will update the accessed and modified timestamps.

To create a text file that you intend to modify straight away, such as a new config file, you can type the command for your favourite editor followed by the path to the file. This will open the editor in a state where saving or writing out the file will save to the path you specify.

```$ vim /path/to/file```

```$ nano /path/to/file```

### Create a new directory

To create a new directory, use the `mkdir` command.

```$ mkdir [<OPTIONS>] /path/to/directory```

When creating a new directory its parent directory must already exist. For example, if you try to create `./new_dir/also_new_dir/` and `./new_dir` does not exist then an error will be returned.

```mkdir: cannot create directory ‘./new_dir/also_new_dir/’: No such file or directory```

To create a new directory, and create any parent directories that do not exist, use the `-p` option.

```$ mkdir -p ./new_dir/also_new_dir/```

If `./new_dir/` does not exist then it will be created.

### View the contents of a file

There are many ways to view the contents of text files from the command line. Two of the most commonly used commands are `cat` and `less`

For smaller files (no more than a few lines), use the `cat` command.

```$ cat /path/to/file```

For larger files, the `less` command is more useful, as it allows for scrolling using the cursor keys, as well as `Home`, `End`, `PgUp`, and `PgDn`.

```$ less /path/to/file```

To quit, press `q`.

### Move files or directories

The `mv` command (**M**o**V**e) 

```$ mv [<OPTIONS>] /path/to/source /path/to/destination```

**WARNING**

The `mv` command will overwrite any file that already exists at the destination path. This is known as "clobbering". To avoid this, use the `-n` option. Alternatively, you can use the `-i` option to decide how to handle each file conflict individually. If in doubt, use `-i`.

### Rename a file or directory

There is no dedicated command for renaming files in Linux. Instead the file is moved from one file name to another.

```$ mv [<OPTIONS>] oldname newname```

### Delete a file

rm

### Delete an empty directory

rmdir

### Delete a directory and all of its contents

rm -rf