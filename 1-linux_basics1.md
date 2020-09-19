# Linux Basics 1

## Today 12 Sep 2020

- Check the system OS details with the following two commands
```
lsb_release -a
uname -a
```

- Know in which directory you are currently in using `pwd` command
- Change the directories using `cd` command
- List the files and folders inside a particular folder
  - Either the one in which you are currently in; in this case you can just type `ls`
  - Or in any folder that you would like know its contents; then you specify the folder no matter where you are currently, so that becomes e.g. `ls Desktop/`
- `ls -la` command lists all the files inside a folder
  - First column of this output shows various things and has 10 characters
  - Eg. `drwxr-xr-x` or `-rw-r--r--`
  - `d` in the first char position stands for directory
  - `-` in the first char position stands for file
  - Second char position onwards, there are 3 groups of 3 chars each. First group of 3 are *read/write/executable* permissions for the file/folder owner, abbreviated as `rwx` whereas if a permission is set to off, then it will have `-` again instead of a symbol or alphabet.
  - Same are the second group of permissions represented for group owner.
  - And the third group of permissions are for all other users.
• `chmod` is the command for changing the permissions
• `chmod +x *filename*` means add the executable permission to everybody

<img src="\\E:\attempts_12sep2020\0-to-hero_12sep2020\0-to-hero_12sep2020\images\ls-la.jpg/">
