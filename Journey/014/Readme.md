# Linux Fundamentals - Day 2

## Linux directory
The Linux directory system is like a tree.

- / - "Root", the top of the file system hierarchy
- /bin - binaries or executable programs, machine-readable
- /etc - configuration files, e.g. file that tells to boot in a graphic or text mode
- /home - Home directories, for your own documents, music files, etc.
- /opt - optional software, software that is not bundled with OS
- /tmp - temporary space that is cleared on reboot
- /usr - user related programs
- /var - variable data, things that change often, most notably log files

Application Directory Structures
- /usr/local/some_backup_software/bin
- /usr/local/some_backup_software/etc
- /usr/local/some_backup_software/lib
- /usr/local/some_backup_software/log

- /opt/avg/bin
- /opt/avg/etc
- /opt/avg/lib
- /opt/avg/log

sometimes:
- /etc/opt/myapp
- /opt/myapp/bin
- /opt/myapp/lib
- /var/opt/myapp

sometimes in shared manner:
/usr/local/bin/myapp
/usr/local/etc/myapp.conf
/usr/local/lib/libmyapp.so

or company name:
/opt/acme
/opt/acme/bin
/opt/acme/etc

or company name/product name
/opt/google
/opt/google/chrome
/opt/google/earth
or other variations

Generally, if software not bundled with OS, it should be in /opt or in /usr (/usr/local)

## The Shell

The default user interface to the Linux system.

Graphical User Interface is a graphical shell.

The shell is a program that executes your commands.

Why the Shell?
- more powerful, e.g. you can run a command on multiple files
- it always be there, GUIs change,
- server distribution do not include GUIs

### The Prompt
[user]$ - user  
[user]# - superuser (the root)

You need a root access to do server-wise operations.

### Basic Linux Commands
- ls
- cd 
- pwd
- cat
- echo
- man
- exit
- clear

Linux commands are case-sensitive.

Directory shortcuts

- . - this directory
- .. - the parent dir
- cd - - change to the previous dir