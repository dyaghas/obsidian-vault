#linux_commands

[[Connection]]
[[System information]]
[[Manipulate files]]
[[Search]]
## man - manual for a command or topic explanation

The `man` command in Linux is used to display the manual pages for a command or topic. It provides documentation and usage information for almost all commands, utilities, and system calls in Linux.

The basic syntax of the `man` command is:

```linux
man [options] [command/topic]
```

Some common `man` options are:

-   `-f`: This option displays a brief description of the specified command or topic.
-   `-k`: This option searches the manual pages for a given keyword.
-   `-w`: This option displays the location of the manual page file for a given command or topic.

--------------

## cancel a command

In Linux, you can cancel a running command or process using the `Ctrl + C` key combination. This will send a SIGINT signal to the running command or process, which will typically cause it to terminate.

Note that some long-running commands or processes may not immediately respond to the `Ctrl + C` signal. In such cases, you can try sending a stronger signal using the `kill` command. The `kill` command can be used to send a signal to a running process, causing it to terminate.

The basic syntax of the `kill` command is:

```linux
kill [signal] [process_id]
```

Where `signal` is the signal that you want to send to the process, and `process_id` is the ID of the process that you want to terminate.

The default signal used by `kill` is SIGTERM, which allows the process to perform cleanup tasks before terminating. If the process does not respond to the SIGTERM signal, you can try sending the SIGKILL signal, which immediately terminates the process without allowing it to perform any cleanup tasks.

To send the SIGTERM signal to a process with a specific process ID, you can use the following command:

```linux
kill -15 [process_id]
```

To send the SIGKILL signal to a process with a specific process ID, you can use the following command:

```linux
kill -9 [process_id]
```

-------------------------

## clear - clear terminal

In Linux, the `clear` command is used to clear the terminal screen. When you execute the `clear` command, it will clear the terminal screen, removing all the previous output from the terminal window.

The syntax of the `clear` command is as follows:

```linux
clear
```

----------------

## history - lists up to 500 previously executed commands

```linux
history
```

Some common `history` options are:

-   `-c`: clears the complete history list.
-   `-d`: offset deletes the history entry at the **OFFSET** position.
-   `-a`: appends history lines.

---------------

# uname - Unix Name

The `uname` command in Linux is used to print system information. It stands for "Unix Name".

The basic syntax of the `uname` command is:

```linux
uname [options]
```

Some common `uname` options are:

-   `-a`: This option prints all system information.
-   `-s`: This option prints the system name.
-   `-n`: This option prints the node name (the name of the machine).
-   `-r`: This option prints the kernel release.
-   `-v`: This option prints the kernel version.
-   `-m`: This option prints the machine hardware name.
-   `-p`: This option prints the processor type or "unknown" if it cannot be determined.
-   `-i`: This option prints the hardware platform or "unknown" if it cannot be determined.
-   `-o`: This option prints the operating system name.

-------------------------

## find - search for file or directory

The `find` command in Linux is a powerful command-line tool used to search for files and directories in a specified location. It can search for files based on a variety of criteria, such as name, type, size, and modification time.

The basic syntax of the `find` command is:

```linux
find path [options] expression
```

Where `path` is the location to search for files, `options` are used to customize the behavior of the command, and `expression` specifies the criteria for the search.

Some common `find` options and expressions are:

-   `-name pattern`: This option searches for files and directories with a specific name pattern. For example, to search for all files with the name "example.txt", you can use the following command:

```linux
find /path/to/search -name example.txt
```

`-type type`: This option searches for files and directories of a specific type. The available types are `f` for regular files, `d` for directories, and `l` for symbolic links. For example, to search for all directories in the current directory, you can use the following command:

```linux
find . -type d
```

`-size size`: This option searches for files based on their size. The size can be specified in bytes, kilobytes, or megabytes. For example, to search for all files in the current directory that are larger than 10 megabytes, you can use the following command:

```linux
find . -size +10M
```

`-mtime n`: This option searches for files based on their modification time. The `n` specifies the number of days ago that the file was modified. For example, to search for all files in the current directory that were modified more than 7 days ago, you can use the following command:

```linux
find . -mtime +7
```

The `find` command can also be combined with other commands and tools to perform more complex operations. For example, you can use the `find` command to search for a specific file, and then pipe the results to another command to perform an action on those files.

Note that the `find` command can be resource-intensive, especially if you are searching a large directory tree. Therefore, it is important to use the command with care and specify the search criteria as precisely as possible to avoid searching unnecessary files and directories.

------------------

## echo

In Linux, the `echo` command is used to display text or variables to the standard output (usually the terminal).

The syntax of the `echo` command is as follows:

```linux
echo [options] [text or variables]
```

Here are some common options that can be used with the `echo` command:

-   `-n`: Do not output the trailing newline character.
-   `-e`: Enable interpretation of backslash escapes in the text.

To display the value of a variable, you can use the following syntax:

```linux
echo $VAR
```

-------------

## cat - concatenate

The `cat` command in Linux is a command-line tool that is used to display the contents of one or more files on the terminal. The name `cat` stands for "concatenate", which means to link together.

The basic syntax of the `cat` command is:

```linux
cat [options] [file(s)]
```

Where `options` are used to customize the behavior of the command, and `file(s)` specifies the name of the file(s) whose contents you want to display. If no file name is specified, `cat` will read input from the standard input.

Some common `cat` options are:

-   `-n`: This option numbers all the output lines.
-   `-b`: This option numbers only the non-blank output lines.
-   `-s`: This option squeezes multiple consecutive blank lines into a single line.
-   `-v`: This option displays non-printing characters as visible characters.

To display the contents of a file, you can simply use the `cat` command followed by the file name, like this:

```linux
cat filename
```

If you want to display the contents of multiple files, you can specify their names separated by spaces, like this:

```linux
cat file1 file2 file3
```

You can also use wildcards to display the contents of all files that match a specific pattern, like this:

```linux
cat *.txt*
```

In addition to displaying the contents of a file, the `cat` command can also be used to combine the contents of multiple files into a single file. To do this, you can use the `>` operator to redirect the output to a new file, like this:

```linux
cat file1 file2 file3 > combined_file
```

This command will concatenate the contents of `file1`, `file2`, and `file3`, and save the result in a new file named `combined_file`.

------------------------