#git

Related:
[[Local changes]]
[[Remote changes]]

## log

`git log` is used to view the commit history of a repository. The command displays a list of all commits made to the repository, along with some metadata about each commit.

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

## branch

`git branch` is a command in Git that is used to manage branches in a Git repository. Branches allow you to work on different versions of a project simultaneously, without affecting the main codebase. You can create a new branch from an existing one, make changes to the new branch, and merge those changes back into the original branch when you're ready.

Here are some common `git branch` commands:

-   `git branch`: lists all the branches in the repository. The current branch is indicated with an asterisk.

-   `git branch <branch-name>`: creates a new branch with the specified name, based on the current branch.

-   `git branch -d <branch-name>`: deletes the specified branch. This command will only delete the branch if all changes in the branch have been merged into the current branch.

-   `git branch -D <branch-name>`: deletes the specified branch, regardless of whether changes in the branch have been merged into the current branch.

-   `git branch -m <new-branch-name>`: renames the current branch to the specified name.


When creating a new branch, you can specify a starting point by providing a commit hash or branch name. For example, to create a new branch called `feature` based on the `main` branch, you can run:

```git
git branch feature main
```

------------------

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

