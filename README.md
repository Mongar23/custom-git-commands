# Custom git commands
This is a collection of new git commands which each have a series of git commands which are often used after eachother.

Use with caution they don't have any fail saves (yet)!

## Table of Contents
- [Usage](#usage)
 - [Linux bash](#linux_bash)
 - [Windows MINGW64](#windows_mingw64)
 - [Windows GitKraken](#windows_gitkraken)
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
Adding the commands to the GitKraken terminal on Windows takes quite some digging, for as far as tested the change can only be made perminently. 
Navigate to the GitKraken install location which is the the `C:\Users\<USER_NAME>\AppData\Local\gitkraken` folder. Once there navigate to `app-<CURRENT_VERSION>\resources\app.asar.unpacked\resources\cli\win\GKPrompt` and add `$env:Path += ";<PATH_TO_REPOSITORY>"` to the top of the `Prompt` function. 

## Commands

### git-remote-branch

### git-commit-push

### git-finish-branch

### git-delete-branch

## TODO
