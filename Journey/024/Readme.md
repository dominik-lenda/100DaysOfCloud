# Linux

## Comparing files

```bash
# compare two files
diff file1 file2

# side-by-side comparison
sdiff file1 file2

# highlighting differences in vim
vimdiff file1 file2
```

### diff output

```bash
diff file1 file2
# first 4 means that both files have 4 lines; c4 means that fourth line is different
4c4
< This is a line in a file.
---
> This is a line in a File!
```
LineNumFile1-Action-LineNumFile2

Action=(a)dd or (c)hange or (d)elete

## Searching in files and using pipes

### The grep command

grep - display lines matching a pattern

The structure:
grep pattern file  
-i Perform a search, ignoring case.  
-c Count the number of occurances in a file.  
-n Precede output with line numbers.  
-v Invert Match. Print lines that don't match.  

### The file command

file file_name display file type.

### Searching for text in binary files

strings - comannd that displays printable strings.

### Pipes

| Pipe symbol

command-output | command-input

Pipe chaines two commands. Pipe takes stdout from the preceding command and passes it as a stdin to fhe following command.

```bash
# result of those two commands is the same
grep pattern file
cat file | grep pattern
```

### The cut command

cut \[file\] Cut out selected portions of file.  
\-d delimiter Use delimiter as the file separator.  
\-f N Display the Nth field


### Example of the pipe
Example of the pipe that gets my user name and real name from /etc/passws and shows it in a clear, formatted way:  

```bash
grep dominik /etc/passwd | cut -d: -f1,5 | tr ":" " " | tr "," " " | column -t
```

### Piping output to a pager

- more
- less

# I did a hands-on lab on working with Azure App Service using Azure CLI

https://cloudacademy.com/lab/working-with-azure-app-service-using-azure-cli/
