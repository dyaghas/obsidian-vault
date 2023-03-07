#git

## add

`git add` is a command in Git that is used to add changes to the staging area. When you make changes to files in a Git repository, those changes are not automatically tracked. Instead, you need to explicitly tell Git which changes you want to include in the next commit. This is where `git add` comes in.

To add changes to the staging area, use the `git add` command followed by the name of the file(s) you want to add. For example, to add changes to a file called `myfile.txt`, you can run:

```git
git add myfile.txt
```

If you want to add all changes in the current directory and its subdirectories, you can use a dot `.` as a wildcard:

```git
git add .
```

Once you have added changes to the staging area, you can use the `git commit` command to create a new commit with those changes. Note that changes in the staging area are not part of any branch yet, and you can modify them by using `git add` again to stage additional changes or `git reset` to unstage changes.

------------

## commit

`git commit` is a command in Git that is used to create a new commit in the repository. A commit represents a snapshot of the repository at a particular point in time and includes a message describing the changes that were made.

To create a new commit, first make sure that you have added the changes you want to include in the commit to the staging area using `git add`. Then, use the `git commit` command followed by the `-m` option and a message describing the changes you made. For example, to create a new commit with the message "Update README.md", you can run:

```git
git commit -m "Update README.md"
```

You can also use the `-a` option to automatically stage any changes to files that are already tracked by Git and then commit them. For example:

```git
git commit -a -m "Update README.md"
```

This is a convenient shortcut if you have made changes to multiple files and want to commit them all at once.

Once you have created a commit, it becomes part of the Git repository's commit history. You can use `git log` to view the commit history and `git show <commit>` to view the details of a specific commit. It's a good practice to write clear and descriptive commit messages that explain the changes you made, as this makes it easier for others (and your future self!) to understand the history of the project.

----------------

## log

`git log` is a command in Git that is used to view the commit history of a repository. The command displays a list of all commits made to the repository, along with some metadata about each commit.

Here are some common options you can use with `git log`:

-   `-n <limit>`: Shows only the last `<limit>` commits.
-   `--oneline`: Displays each commit on a single line, showing only the commit hash and the first line of the commit message.
-   `--graph`: Shows the commit history as a graph, with branches and merges clearly displayed.
-   `--author=<name>`: Shows only the commits made by the specified author.
-   `--since=<date>`: Shows only the commits made since the specified date.

You can also use `git log` with additional arguments to filter the commit history based on certain criteria, such as a specific file or directory. For example, to view the commit history for a specific file, you can run:

```git
git log myfile.txt
```

--------------

## reset

`git reset` is a command in Git that is used to reset the current state of the repository to a previous commit. This can be useful if you need to undo changes or go back to a previous version of the code.

Here are some common uses of `git reset`:

1.  Resetting the staging area: To unstage changes that you have added to the staging area, use the `git reset` command followed by the name of the file(s) you want to unstage. For example, to unstage changes to `myfile.txt`, you can run:
```git
git reset myfile.txt
```

If you want to unstage all changes in the staging area, you can use a dot `.` as a wildcard:

```git
git reset .
```

2.  Undoing changes: To undo changes you have made to a file since the last commit, use the `git reset` command followed by the name of the file(s) you want to reset. Note that this only affects the working directory and does not create a new commit.

3.  Moving the HEAD pointer: To reset the repository to a previous commit, use the `git reset` command followed by the SHA-1 hash of the commit you want to reset to. For example, to reset the repository to the commit with the hash `abc123`, you can run:

```git
git reset abc123
```

By default, this will move the HEAD pointer and the current branch pointer to the specified commit, effectively "undoing" any commits that came after it. This can be a dangerous operation, as it permanently removes any changes that were made in those commits.

Note that there are different modes of `git reset` that can have different effects on the repository state. The most common modes are `--mixed` (default), `--soft`, and `--hard`. It's important to be careful when using `git reset`, as it can permanently delete changes that have not been committed.

------------

## push

-----------------------

## pull

-------------

## checkout

The `git checkout` command is used to switch between different branches or to move the current working directory to a specific commit in Git.

To switch to an existing branch, use `git checkout` followed by the name of the branch you want to switch to:

```git
checkout <branchname>
```

If you want to create a new branch and switch to it at the same time, use the `-b` option followed by the name of the new branch:

```git
git checkout -b <newm_branchname>
```

To move to a specific commit, use `git checkout` followed by the commit hash (a commit ID):

```git
git checkout <commit_hash>
```

This will detach your `HEAD` from any branch, meaning that any changes you make will not be associated with a branch. To switch back to a branch, simply run `git checkout` followed by the branch name.

Note that when you use `git checkout` to switch to a different branch or commit, Git will overwrite your working directory with the contents of the branch or commit you're switching to. Therefore, any changes that you've made to your files that are not yet committed will be lost. Be sure to commit your changes before switching to a different branch or commit.

-------------

## branch



------------------