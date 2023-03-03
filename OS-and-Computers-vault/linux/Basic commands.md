#linux_commands

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

## useradd

The `useradd` command is a Linux command used to create a new user account. It is usually used with root privileges, as only the root user can create new user accounts on a system.

The basic syntax of the `useradd` command is:

```linux
useradd [options] username
```

Some common options used with `useradd` are:

-   `-m`: Creates a home directory for the new user.
-   `-s`: Specifies the default shell for the new user.
-   `-G`: Adds the new user to one or more secondary groups.

For example, to create a new user named "john" with a home directory and the bash shell, you can use the following command:

```linux
sudo useradd -m -s /bin/bash john
```

After running this command, you should set a password for the new user with the `passwd` command:

```linux
sudo passwd john
```

------------

## passwd - password

The `passwd` command in Linux is used to change the password of a user account. By default, the `passwd` command can only be run by the root user or by the user who owns the account.

The basic syntax of the `passwd` command is:

```linux
passwd [options] [ username]
```

The `passwd` command also provides various options that you can use to customize its behavior. Some common options include:

-   `-l`: Locks the password of the specified user account.
-   `-u`: Unlocks the password of the specified user account.
-   `-d`: Deletes the password of the specified user account.
-   `-S`: Displays the status of the password for the specified user account.

------------

## su - switch user

The `su` command in Linux is used to switch to another user account or to run a command with a different user's permissions. By default, the `su` command allows you to switch to the root user account, but you can also switch to other user accounts if you have the necessary permissions.

The basic syntax of the `su` command is:

```linux
su [options] [username]
```

Where `username` is the name of the user account that you want to switch to. If you do not specify a username, the `su` command will switch to the root user account by default.

To switch to the root user account, you can simply run the `su` command without any arguments:

-----------------------

## ssh

The SSH command in Linux is used to establish a secure encrypted connection between two systems over an insecure network. SSH stands for "Secure Shell" and it is a network protocol that provides a secure way to access remote systems.

The syntax of the SSH command in Linux is as follows:

```linux
ssh [options] [user@]hostname [command]
```

Here, `[options]` are any command-line options you want to pass to the SSH command. `[user@]hostname` specifies the remote system you want to connect to. If you don't specify a username, the command will use your local username. Finally, `[command]` is an optional command to execute on the remote system after connecting.

For example, to connect to a remote system with the hostname "example.com" using the default username and run the command "ls -l" on the remote system, you can use the following SSH command:

```linux
ssh example.com ls -l
```

When you run the command, SSH will prompt you for the password for the remote system's user account. If you have set up SSH key-based authentication, you may not need to enter a password. Once you enter the correct password, the SSH command will establish a secure connection and run the specified command on the remote system.

-----------

## clear - clear terminal

In Linux, the `clear` command is used to clear the terminal screen. When you execute the `clear` command, it will clear the terminal screen, removing all the previous output from the terminal window.

The syntax of the `clear` command is as follows:

```linux
clear
```

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

[[commands - manipulate files]]
[[commands - search]]