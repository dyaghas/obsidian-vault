#linux_commands 

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

----------

## ping - check if a network or a server is reachable

The `ping` command in Linux is a command-line tool that is used to test the connectivity between two devices over a network. It sends an Internet Control Message Protocol (ICMP) echo request packet to the specified destination and waits for a response.

The basic syntax of the `ping` command is:

```linux
ping [options] destination
```

ome common `ping` options are:

-   `-c`: This option specifies the number of packets to send.
-   `-i`: This option specifies the time interval between packets.
-   `-s`: This option specifies the size of the packets.
-   `-t`: This option specifies the Time To Live (TTL) value for the packets.

-------------------

The `wget` command in Linux is a command-line tool that is used to download files from the Internet. It supports various protocols such as HTTP, HTTPS, and FTP, and can be used to download files recursively.

The basic syntax of the `wget` command is:

```linux
wget [options] URL
```

Some common `wget` options are:

-   `-O`: This option specifies the name of the output file.
-   `-c`: This option continues an interrupted download.
-   `-r`: This option downloads files recursively.
-   `-np`: This option prevents `wget` from following links to parent directories.
-   `-P`: This option specifies the directory where downloaded files will be saved.

-----------------