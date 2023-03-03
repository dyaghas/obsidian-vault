#linux_commands 

## touch - create file

In Linux, the `touch` command is used to create new files or update the timestamps on existing files. It is a basic command that is often used in the command-line interface to create empty files or update the modification and access times of existing files.

The syntax of the `touch` command is as follows:

```linux
touch [options] [file]
```

Here are some common options that can be used with the `touch` command:

-   `-c`: Do not create a new file if the file does not exist.
-   `-t`: Use a specific time stamp instead of the current time. The time stamp should be specified in the format `[[CC]YY]MMDDhhmm[.ss]`.

For example, to create a new file named `myfile.txt`, you can use the following command:

```linux
touch myfile.txt
```

This command will create a new empty file named `myfile.txt` in the current directory. If the file already exists, the `touch` command will update the modification and access times of the file.

----------

## nano - create and edit file

In Linux, the `nano` command is a text editor that is often used in the command-line interface to create and edit files. It is a lightweight and user-friendly text editor that is ideal for quick edits and simple text manipulation.

The syntax of the `nano` command is as follows:

```linux
nano [options] [file]
```

When you open a file with the `nano` command, the text editor will display the contents of the file in the terminal window. You can then use the keyboard to make changes to the text, save the file, or exit the editor.

Here are some common keyboard commands that you can use in `nano`:

-   `Ctrl-O`: Save the changes to the file.
-   `Ctrl-X`: Exit the editor.
-   `Ctrl-K`: Cut the current line.
-   `Ctrl-U`: Uncut the last cut line.
-   `Ctrl-W`: Search for a specific string of text.
-   `Ctrl-\`: Replace a string of text with another string.
-   `Ctrl-A`: Select all text.
-   `Ctrl-C`: Display the current cursor position.

In addition to these keyboard commands, `nano` also supports various command-line options that you can use to customize the editor. For example, you can use the `-w` option to disable word wrapping, or the `-c` option to display line numbers.

---------------

## vim - create and edit file

In Linux, the `vim` command is a text editor that is often used in the command-line interface to create and edit files. It is a powerful and versatile text editor that can be customized to suit the needs of individual users.

The `vim` editor has a variety of modes that are used for different tasks. The two main modes are the command mode and the insert mode. In the command mode, you can use keyboard commands to perform tasks such as saving the file, searching for text, and moving the cursor. In the insert mode, you can type text into the editor.

The syntax of the `vim` command is as follows:

```linux
vim [options] [file]
```

When you open a file with the `vim` command, the text editor will display the contents of the file in the terminal window. By default, `vim` will start in the command mode. To start typing text, you need to switch to the insert mode by pressing the `i` key.

Here are some common keyboard commands that you can use in `vim`:

-   `:w`: Save the changes to the file.
-   `:wq`: Save the changes and exit the editor.
-   `:q`: Exit the editor.
-   `:q!`: Exit the editor without saving changes.
-   `/text`: Search for the string `text` in the file.
-   `:s/old/new/g`: Replace all occurrences of `old` with `new` in the file.
-   `yy`: Copy the current line.
-   `p`: Paste the copied line.
-   `dd`: Delete the current line.
-   `u`: Undo the last change.
-   `Ctrl-G`: Display the current cursor position.

In addition to these keyboard commands, `vim` also supports various command-line options that you can use to customize the editor. For example, you can use the `-c` option to execute a command when the editor is started, or the `-n` option to disable line numbers.

---------------

## shred - destroy file data

In Linux, the `shred` command is a utility that is used to securely delete files by overwriting the contents of the file multiple times with random data. The purpose of the `shred` command is to ensure that the deleted data cannot be recovered by any means.

The syntax of the `shred` command is as follows:

```linux
shred [options] file
```

By default, the `shred` command overwrites the contents of the file 3 times with random data. This is considered sufficient to make the data unrecoverable by any means. However, you can use the `-n` option to specify the number of times the file should be overwritten.

Here are some common options that you can use with the `shred` command:

-   `-n`: Specify the number of times the file should be overwritten. For example, `-n 10` will overwrite the file 10 times with random data.
-   `-v`: Verbose mode. Display the progress of the operation.
-   `-z`: Zero the contents of the file after it has been shredded.

For example, to securely delete a file named `myfile.txt` using the `shred` command, you can use the following command:

```linux
shred -n 3 -vz myfile.txt
```

This command will overwrite the contents of the file `myfile.txt` 3 times with random data, display the progress of the operation, and then zero the contents of the file. After this operation, the file will be securely deleted and the data it contained will be unrecoverable.

--------------------

- ## cp - copy file or directory

In Linux, the `cp` command is a utility that is used to copy files and directories. The `cp` command takes the source file or directory and creates a new file or directory with the same contents.

The syntax of the `cp` command is as follows:

```linux 
cp [options] source destination
```

By default, the `cp` command copies only the files, not directories. If you want to copy directories, you need to use the `-r` option, which stands for "recursive". This option copies the directory and all of its contents, including other directories and files.

Here are some common options that you can use with the `cp` command:

-   `-r`: Copy directories recursively.
-   `-i`: Prompt before overwriting an existing file.
-   `-v`: Verbose mode. Display the progress of the operation.

------------------

## mv - move file or directory

In Linux, the `mv` command is a utility that is used to move or rename files and directories. The `mv` command takes the source file or directory and moves it to a new destination or renames it.

The syntax of the `mv` command is as follows:

```linux
mv [options] source destination
```

If you want to move the file or directory to a new location, you can specify the new path as the `destination`. If you want to rename the file or directory, you can specify the new name as the `destination`.

Here are some common options that you can use with the `mv` command:

-   `-i`: Prompt before overwriting an existing file.
-   `-u`: Move the file only if the source is newer than the destination.
-   `-v`: Verbose mode. Display the progress of the operation.

For example, to move a file named `myfile.txt` to a new location named `myfolder/myfile.txt`, you can use the following command:

```linux
mv myfile.txt myfolder/myfile.txt
```

This command will move the file `myfile.txt` to the directory `myfolder` and rename it to `myfile.txt`.

To rename a file named `oldname.txt` to `newname.txt`, you can use the following command:

```linux
mv oldname.txt newname.txt
```

----------------

## rm - remove file or directory

In Linux, the `rm` command is used to remove or delete files and directories. The `rm` command removes the specified files or directories from the file system.

The syntax of the `rm` command is as follows:

```linux
rm [options] file1 file2...
```

By default, the `rm` command does not remove directories. If you want to remove a directory and all of its contents, you need to use the `-r` option, which stands for "recursive". This option removes the directory and all of its contents, including other directories and files.

Here are some common options that you can use with the `rm` command:

-   `-i`: Prompt before deleting each file.
-   `-f`: Force deletion without prompting for confirmation.
-   `-r`: Recursively delete directories and their contents.
-   `-v`: Verbose mode. Display the progress of the operation.

-------------

## mkdir - Make directory

The `mkdir` command in Linux is a command-line tool that is used to create new directories (folders) on the file system.

The basic syntax of the `mkdir` command is:

```linux
mkdir [options] directory_name(s)
```

Some common `mkdir` options are:

-   `-p`: This option creates intermediate directories if they do not exist. For example, if you want to create a directory `/home/user1/newdir`, but the `user1` directory does not exist, you can use the following command:

```linux
mkdir -p /home/user1/newdir
```

`-m`: This option sets the permissions of the new directory. You can specify the permissions in octal notation (e.g. `755`) or symbolic notation (e.g. `u+rwx,g+rx,o+rx`). For example, to create a directory with permissions `rwxr-xr-x`, you can use the following command:

```linux
mkdir -m 755 newdir
```

`-v`: This option displays a message for each directory that is created.

If you want to create multiple directories at once, you can specify their names separated by spaces, like this:

```linux
mkdir dir1 dir2 dirn...
```

If you want to create a directory with a specific path, you can specify the path using the forward slash (`/`) as the directory separator, like this:

```linux
mkdir path/to/directory
```

If any of the directories in the path do not exist, you can use the `-p` option to create them.

--------------------------

## ln - link

In Linux, the `ln` command is used to create links between files or directories. A link is a reference to a file or directory that allows you to access the file or directory from a different location in the file system.

There are two types of links that can be created using the `ln` command:

1.  Hard links: A hard link is a reference to a file or directory that points to the same physical location on disk as the original file or directory. When you create a hard link, you essentially create a new name for the file or directory. If you delete the original file or directory, the hard link will still point to the same physical location on disk.

2.  Symbolic links: A symbolic link, also known as a soft link, is a reference to a file or directory that points to the path of the original file or directory. When you create a symbolic link, you essentially create a shortcut to the original file or directory. If you delete the original file or directory, the symbolic link will become invalid.


The syntax of the `ln` command is as follows:

```linux
ln [options] source_file target_file
```

If you want to create a hard link, you can use the `-f` option, which stands for "force". For example, to create a hard link to a file named `myfile.txt`, you can use the following command:

```linux
ln -f myfile.txt mylink
```

This command will create a hard link named `mylink` that points to the same physical location on disk as the original file `myfile.txt`.

If you want to create a symbolic link, you can use the `-s` option, which stands for "symbolic". For example, to create a symbolic link to a file named `myfile.txt`, you can use the following command:

```linux 
ln -s myfile.txt mylink
```

This command will create a symbolic link named `mylink` that points to the path of the original file `myfile.txt`.

Note that creating links between files or directories can be a useful way to organize files and directories in the file system, but it can also lead to confusion and errors if not used carefully.

----------

## apt

The `apt` command in Linux is a package manager used to manage software packages on Debian and Ubuntu systems. It is a command-line tool that allows you to search for, install, update, and remove software packages.

The basic syntax of the `apt` command is:

```linux
apt [options] command
```

Where `command` is the action that you want to perform, such as `install`, `remove`, `update`, or `search`. The `options` are used to customize the behavior of the command.

Some common `apt` commands and their usage are:

-   `apt-get update`: This command updates the local package database, which contains information about the available software packages and their versions.
-   `apt-get upgrade`: This command upgrades the installed software packages to their latest versions.
-   `apt-get install package_name`: This command installs a new software package named `package_name`.
-   `apt-get remove package_name`: This command removes an installed software package named `package_name`.
-   `apt-get autoremove`: This command removes all the dependencies that were installed with a software package that is no longer needed by any other installed package.
-   `apt-cache search package_name`: This command searches for software packages that match the specified `package_name`.

Note that the `apt` command requires root or superuser privileges to perform certain actions, such as installing or removing software packages. Therefore, you should run the `apt` command with the `sudo` command, like this:

```linux
sudo apt-get [optinos] command
```

This will prompt you for your user password, and then execute the command with elevated privileges.

-------------

## zip - compress files

The `zip` command in Linux is used to compress files and directories into a single ZIP archive. It is a popular command-line tool for creating and managing compressed archives in Linux.

The basic syntax of the `zip` command is:

```linux
zip [options] archive.zip file1 file2 dir1 dir2
```

Some common `zip` options are:

-   `-r`: This option tells `zip` to include all files and subdirectories in the specified directories in the archive recursively.
-   `-q`: This option tells `zip` to operate in quiet mode, without displaying any status messages.
-   `-9`: This option tells `zip` to use the maximum compression level (best compression) when creating the archive.

-------------

## tar - compress files

The `tar` command in Linux is a command-line tool that is used to create and manipulate tar archives, which are a type of compressed archive that can contain multiple files and directories (**similar to ZIP in Windows**).

The basic syntax of the `tar` command is:

```linux
tar [options] archive files/directories
```

Some common `tar` options are:

-   `-c`: This option creates a new archive.
-   `-x`: This option extracts the contents of an archive.
-   `-v`: This option displays verbose output, which shows the progress of the operation and the files being processed.
-   `-f`: This option specifies the name of the archive file.
-   `-z`: This option compresses the archive using gzip.
-   `-j`: This option compresses the archive using bzip2.

To create a new archive, you can use the `tar` command like this:

```linux
tar -cvf archive.tar files/directories
```

If you want to extract the contents of an archive, you can use the `tar` command like this:

```linux
tar -xvf archive.tar
```