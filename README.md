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

## Start Tracking the Files

**git bash**
1. Type
    ```
    $ git add README.md
    ```
1. `git status` command now shows
that `README.md` file is in the `Changes to be committed` section
and indicated as `new file`.

**Sourcetree**
1. In the `Unstaged files` section,
click the `+` button at the far right of `README.md` file.
1. Now, `README.md` file is in `Staged files` section.

Now, the files begin to be tracked by git,
but are not accepted as a version yet.
In order to be a version, *commit* action is necessary.

## Commit

**git bash**
1. Type
    ```
    $ git commit -m '<commit_message>'
    ```
1. `git status` command now says
"nothing to commit, working tree clean".
1. Commit history can be shown by
    ```
    $ git log
    ```

**Sourcetree**
1. Click `Commit` in the toolbar.
1. Write `<commit_message>` in the box at the bottom of the window.
1. Commit history is shown by selecting `WORKSPACE - History` at the sidebar

## Stage

## To be studied more

`?? README.md`

`git -rm --cached <file>...` to unstage