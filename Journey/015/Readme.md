# Linux 2/n

## Long listing
- $ ls -l - detailed 
- $ ls -a - show hidden files (all files)
- $ ls -al or $ ls -la - combine
- $ ls -F - reveal file type (/ - ; @ - link; * - executable)
- $ ls -F - reveal file type (/ - ; @ - link; * - executable)
- $ ls -latr - list all files, ordered by time, reversed (last-modified on the bottom)
- ls -R - list recursively
- tree -d - visualize  directory tree
- tree -C - colorize visualization of directory tree
### What is a link?
Symbolic links are pointers to the actual file or directory.

Link is used as if it were the file.

Foir example, it is a shortcut for long names of files or directories

## File and Directory Permissions

### Permissions
Example:
drwxrwxr-x

Type:
- - - regular file
- d - directory
- l - symbolic link

Permission:
r - read
w - write
x - execute

Difference in permissions between files and directories:

| Permission | File             | Directory                           |
|------------|------------------|-------------------------------------|
| r          | Can be read      | Files in the directory can be read  |
| w          | Can be modifieds | You can edit files in the directory |
| x          | Can be executed  | Gives access to metadata            |

Permission Categories
- u - user (owner of the file)
- g - group (the members of the files)
- o - other (all users)
- a - all

Every user belongs to at least one group.

`groups`
`id -Gn`


