#git

## add

------------

## commit

--------------

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