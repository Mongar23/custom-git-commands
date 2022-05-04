# Custom git commands
This is a collection of new git commands which each have a series of git commands which are often used after each other.

Use with caution they don't have any fail saves (yet)!

## Table of Contents
- [Usage](#usage)
 - [Linux bash](#linux-bash)
 - [Windows MINGW64](#windows-mingw64)
 - [Windows GitKraken](#windows-gitkraken)
- [Commands](#commands)
	- [git-remote-branch](#git-remote-branch)
	- [git-commit-push](#git-commit-push)
	- [git-finish-branch](#git-finish-branch)
	- [git-delete-branch](#git-delete-branch)
- [TODO](#todo)

## Usage
To be able to use the commands you will need to add the cloned repository direction to the shell's path variable. These are the ways that are currently tested and working.

### Linux bash
For a one time use case type `export PATH=$PATH:<PATH_TO_REPOSITORY>` in the terminal. To access the commands permanently add `export PATH=$PATH:<PATH_TO_REPOSITORY>` to the `.bashrc` file which path is `~/.bashrc`.

### Windows MINGW64
For a one time use case type `export PATH=<PATH_TO_REPOSITORY>:$PATH` in the terminal.
To make it permanent navigate to `C:\Users\<USER_NAME>` add `export PATH=<PATH_TO_REPOSITORY>:$PATH` to the `.bash_profile`. if the `.bash_profile` file does not exists, create it.

### Windows GitKraken
In linux using the commands in the gitkraken terminal is simple it just uses the `.bashrc` file like explained in [Linux bash](#linux-bash). Adding the commands to the GitKraken terminal on Windows however, takes quite some digging, for as far as tested the change can only be made permanently. 
Navigate to the terminal config file which is located in this folder: 
```
C:\Users\<USER_NAME>\AppData\Local\gitkraken\app-<CURRENT_VERSION>\resources\app.asar.unpacked\resources\cli\win\GKPrompt
```
Edit the `GKPrompt.psm1` file, and add `$env:Path += ";<PATH_TO_REPOSITORY>"` to the top of the `Prompt` function.

## Commands
### git-remote-branch
```shell
git remote-branch <BRANCH_NAME>
```
This will create a new branch, check it out, and push it to the origin with the `--set-upstream` flag.

### git-commit-push
```shell
git commit-push <"COMMIT_MESSAGE">
```
This will stage all the current changes with `git add *`, commit them, and push it to the origin.
Note: the message argument needs the `'` or `"` for it to work, just like `git commit -m`.

### git-finish-branch
```shell
git finish-branch <MERGING_BRANCH:current_branch> <RECEIVING_BRANCH:development>
```
This will checkout the `RECEIVING_BRANCH`, merge the `MERGING_BRANCH` into the `RECEIVING_BRANCH` with the `--no-ff` flag and the message `merged 'MERGING_BRANCH' into RECEIVING_BRANCH`, push it to the origin of the `RECEIVING_BRANCH`, and finally delete the `MERGING_BRANCH` locally and remotely. 

The first argument is the branch which needs to be merged, it has a default value of the branch where the command is started from.
The second argument is the branch where the merging branch is merged into, it has a default value of the `development`.

### git-delete-branch
```shell
git delete-branch <BRANCH_TO_DELETE> <CHECKOUT_BRANCH:development>
```
This will checkout to `CHECKOUT_BRANCH`, delete `BRANCH_TO_DELETE` locally, push to the origin of `BRANCH_TO_DELETE` with the `-d` flag, to delete it remotely.

## TODO
- [ ] Test and add fail saves to the `git-finish-branch` command.
- [ ] Test and add fail saves to the `git-delete-branch` command.
- [ ] Add a init with and with origin command.
