# Introductory Terminal Commands

## Basic Commands

**Navigating**

- `pwd`: Print Working Directory - shows the current directory.
- `ls`: List - displays files and directories in the current directory.
- `cd <directory>`: Change Directory - moves to the specified directory. Use `cd ..` to go up one directory level. `.` represents the current directory, and `..` represents the parent directory.
- `cd ~` to change directory to the root of current user
- `cd ..` to change directory to the parent folder
- `cd ../..` to change directory to the parent's parent folder (keep concatenating ..)

**Files & Folders**

- `mkdir <directory>`: Make Directory - creates a new directory.
- `rmdir <directory>`: Remove Directory - deletes an empty directory.
- `rm <file>`: Remove - deletes a file.
- `cp <source> <destination>`: Copy - copies files or directories.
- `mv <source> <destination>`: Move/Rename - moves or renames files/directories.
- `touch <file>`: Touch - creates a new empty file or updates a file's timestamp.
- `cat <file>`: Concatenate - displays the contents of a file.

**Help & Other**

- `man <command>`: Manual - displays the manual page for a command.
- `<command> -h`: Help - displays the help page for a command.
- `exit`: Exit - closes the terminal session.

## Git Commands

- `git init`: Initialize a new Git repository in the current directory.
- `git clone <repository>`: Clone a Git repository from a remote source (this creates a folder).
- `git clone . <repository>`: Clone a Git repository from a remote source in the current folder (this does not create a folder).
- `git add .`: Stage all files for commit.
- `git add <file>`: Stage specific file for commit.
- `git commit -m "message"`: Commit staged changes with a descriptive message.
- `git status`: Show the status of your Git repository.
- `git log`: Display the commit history.
- `git branch`: List branches in the repository.
- `git branch <branch>`: Creates a new branch in the repository.
- `git checkout <branch>`: Switch to a different branch.
- `git merge <branch>`: Merge changes from one branch into the current branch.
- `git pull`: Fetch and merge changes from a remote repository.
- `git push`: Push local changes to a remote repository.

**Diff**

- `git diff`: Compare changes between the working directory and the most recent commit.
- `git diff <commit1> <commit2>`: Compare changes between two specific commits.
- `git diff <file>`: Compare changes in a specific file.

**Selective Line Commit**

Sometimes, you may want to commit only specific lines or changes within a file:

1. Use `git diff` to view the changes and identify the lines you want to commit.
2. Copy the relevant lines or changes from the `git diff` output.
3. Create a new branch or ensure you are on the correct branch.
4. Use `git add -p` to interactively stage changes.
5. Select which changes to stage and commit them using `git commit`.
6. Your commit will include only the selected lines or changes.

## Vim Commands

- `vim <file>`: Open Vim editor to edit a file.
- In Vim, press `i` to enter insert mode, `Esc` to exit insert mode, `:w` to save changes, and `:q` to quit Vim.
- `:wq`: Save changes and quit Vim.
- `:q!`: Quit Vim without saving changes.

## Terminal Shortcuts (Mac)

- `Ctrl + C`: Cancel the current command.
- `Ctrl + L` (or `Command + K`): Clear the terminal screen.
- `Ctrl + A`: Move cursor to the beginning of the line.
- `Ctrl + E` (or `Command + E`): Move cursor to the end of the line.
- `Ctrl + U`: Delete the line.
- `Ctrl + W`: Delete the word before the cursor.
- `Ctrl + R` (or `Command + R`): Search through command history.
- `Tab`: Auto-complete files, directories, and command names.
- Hold `Alt` (or `Option`) and click to put cursor at certain location
- `Up/Down Arrow`: Scroll through command history.

## Example Git Workflow

This is just an example for the lecture of how someone would go about navigating files with the terminal and set up project in github. It's better to understand each line of commands rather than just run them. This example includes the idea that you might make a mistake moving to the wrong directory and then use the `../` to change directory back to a parent directory.

```bash
cd ~/user_folder
cd desired_location
cd ../
cd correct_folder
mkdir my_repo
cd my_repo
touch index.js
vim index.js
git init
git add .
git commit -m "first commit"
git push -u origin main
```
