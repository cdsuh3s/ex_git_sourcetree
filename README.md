install sourcetree v3.4.5

## user setup

## Create a new repository

**git bash**
1. Create the directory for new repository and get into it.
1. Type
    ```
    $ git init
    ```

**Sourcetree**
1. Click `Create` in the toolbar.
1. Click `Browse` and choose a directory for a new repository.
1. Click `Create` button below.

A new hidden subdirectory named as `.git` will be created,
which contains the files necessary for the management of git.

## Add New files to be managed by git

Create a file. (e.g. `README.md`)

**git bash**
1. To check the status, type
    ```
    $ git status
    ```
1. `README.md` file can be found in `Untracked Files` section.

**Sourcetree**
1. `README.md` file can be found in `Unstaged files` section with a question mark icon.
1. The question mark icon means the file is *not tracked*.

*Untracked* or *Not Tracked* means the files are in the repository, but not managed by git yet.

## Stage

## Commit
