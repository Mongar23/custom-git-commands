# Custom git commands
This is a collection of new git commands which each have a series of git commands which are often used after eachother.

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
To be able to use the commands you will need to add the cloned repository direction to the shell's path variable. 

### Linux bash
For a one time use case type `export PATH=$PATH:<PATH_TO_REPOSITORY>` terminal. 
In case you want it to be permanent add `export PATH=$PATH:<PATH_TO_REPOSITORY>` to the `.bashrc` file which path is `~/.bashrc`.

### Windows MINGW64
For a one time use case type `export PATH=<PATH_TO_REPOSITORY>:$PATH` in the terminal.
To make it perminent navigate to `C:\Users\<USER_NAME>` add `export PATH=<PATH_TO_REPOSITORY>:$PATH` to the `.bash_profile`. if the `.bash_profile` file doens't exists, create it.

### Windows GitKraken
In linux using the commands in the gitkraken terminal is simple it just uses the `.bashrc` file like explained in[Linux bash](#linux-bash). Adding the commands to the GitKraken terminal on Windows however, takes quite some digging, for as far as tested the change can only be made perminently. 
Navigate to the terminal config file which is located in this folder: 
```
C:\Users\<USER_NAME>\AppData\Local\gitkraken\app-<CURRENT_VERSION>\resources\app.asar.unpacked\resources\cli\win\GKPrompt
```
Edit the `GKPrompt.psm1` file, and add `$env:Path += ";<PATH_TO_REPOSITORY>"` to the top of the `Prompt` function.

## Commands

### git-remote-branch

### git-commit-push

### git-finish-branch

### git-delete-branch

## TODO
