# Version Control System : git with Sourcetree

git
- MS Windows version
- version : 2.92.2
- Homepage : https://www.git-scm.com

Sourcetree
- Version : 3.4.5
- Homepage : https://www.sourcetreeapp.com

## Setup

### Set-up User

**git bash**
```
$ git config --global user.name "<user_name>"
$ git config --global user.email "<email_address>"
```

**Sourcetree**
1. In the menubar, `[Tools] - [Options]`
1. Select `[General]` tab.
1. In `Default user information`,
provide `Full Name` and `Email address`.

### Set-up Editor

**git bash**
- gvim
    ```
    $ git config --global core.editor "'C:\Program Files\Vim\vim82\gvim.exe' --nofork '%*'" 
    ```
- Visual Studio Code
    ```
    $ git config --global core.editor "code --wait"
    ```

### Check Settings

**git bash**
```
$ git config --list
```

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

## Remote Repository

GitHub site will be used.

### Create a Remote Repository

Create a new repository on GitHub.
- public
- empty : no `README`, `.gitignore`, license

### Connect the Local Repository to the Remote Repository

**Sourcetree**
1. In the memubar, `[Repository] - [Add Remote...]`.
1. In the `[Remotes]` tab, `[Add]`.
1. Copy HTTPS address from remote repository page,
Paste it in `[URL / Path]`.
Information in the `[Optional extended integration]` will be changed to reflect GitHub.
1. Check `[Default remote]` checkbox.
`[Remote name]` is set to `origin`.
1. `[OK]`. `[OK]`.
1. In the sidebar, `origin` appears under `[Remote]`.

origin : a kind of nickname for remote repository to make easy to use(call)

### Push

Synchronization, upload

**Sourcetree**
1. In the toolbar, `[Push]`.
1. For `[Push to repository]`, select remote name `origin`.
1. In the `[Branches to push]`,
select the branches to push to the remote repository using checkbox.
1. `[Push]`
1. Visit and check the remote repository page.

## Reference
- https://opentutorials.org

## Memos
- Dropbox, Google Drive are integrated with simple VCS.

## To be studied more

`?? README.md`

`git -rm --cached <file>...` to unstage

## New repository on GitHub

- HTTPS : https://github.com/cdsuh3s/ex_git_sourcetree.git
- SSH : git@github.com:cdsuh3s/ex_git_sourcetree.git

### Create a new repository on the command line
```git
echo "# ex_git_sourcetree" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:cdsuh3s/ex_git_sourcetree.git
git push -u origin main
```

### Push an existing repository from the command line
```git
git remote add origin git@github.com:cdsuh3s/ex_git_sourcetree.git
git branch -M main
git push -u origin main
```