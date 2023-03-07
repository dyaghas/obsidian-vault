#linux_commands 

## top

The `top` command in Linux is used to display system resource usage and process information. It provides a dynamic real-time view of the processes running on a system, including their CPU and memory usage, and allows users to interactively monitor and manage them.

When you run the `top` command, it will display a live-updating list of processes, sorted by their CPU usage by default. The top of the screen shows system-level information, such as the current time, how long the system has been running, and how many users are logged in. The main section of the screen shows the processes that are currently running, along with information about their CPU and memory usage.

Some common interactive commands that can be used while running `top` are:

-   `k`: This command allows you to kill a process by its process ID (PID).
-   `u`: This command allows you to filter the process list by user.
-   `M`: This command sorts the process list by memory usage.
-   `P`: This command sorts the process list by CPU usage.
-   `q`: This command quits `top`.

--------------

## df - disk usage

The `df` command in Linux is a command-line tool that is used to display information about the file system usage on your system.

The basic syntax of the `df` command is:

```linux
df [options] [directory]
```

Some common `df` options are:

-   `-h`: This option displays the output in a human-readable format, with sizes in units like KB, MB, and GB.
-   `-T`: This option displays the type of file system for each mounted file system.
-   `-i`: This option displays the inode usage for each file system.

------------------

## du - disk usage

The `du` command in Linux is a command-line tool that is used to estimate file space usage.

The basic syntax of the `du` command is:

```linux
du [options] [directory]
```

Some common `du` options are:

-   `-h`: This option displays the output in a human-readable format, with sizes in units like KB, MB, and GB.
-   `-s`: This option displays a summary of the total disk usage for the specified directory.
-   `-c`: This option displays a grand total of the disk usage for all specified directories.
-   `-x`: This option tells the `du` command not to cross file system boundaries.

-------------------

