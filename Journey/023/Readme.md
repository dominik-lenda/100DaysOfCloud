# Linux Day 5

## Wildcards
Wildcard is a character or string used for pattern matching.

Wildcards can be used with most commands:
- ls
- rm
- cp

Two main **wildcards**:
- \* - matches zero or more characters
*.txt  
a*
a*.txt
- ? - matches exactly one character
?.txt  
a?  
a?.txt (a5.txt, ak.txt)
https://4651a584-962e-4e31-93f8-7ead63f65b36-code.t.cloudacademylabs.com/#/home/project
### Character Classes
- \[\] - A character class.

Matches any of the characters included between the brackets. Matches exactly one character.

\[aeiou\] - look for file names that has any of the vowels  
ca\[nt\] -> can, cat, candy, catch  

- \[!\] - matches any of the characters NOT included between brackets.
\[!aeiou\]*

### Ranges
- \[a-g\]* or \[1-6\]* 
- \[\[:alpha:\]\]
- \[\[:digit:\]\]
- \[\[:lower:\]\]
- \[\[:space:\]\] - mathces whitespaces - spaces, tabs, etc.
- \[\[:upper:\]\]

### Escaping Wildcards
use \
- *\?
but generally it is better to avoid question marks inside a file name

## Input, Output, and Redirection
- Neither my keyboard, nor monitor is a file. But that's not true. Linux represents everything as a file.

| I/O name        | Abbrevation | File description |
|-----------------|:-----------:|:----------------:|
| Standard input  |    stdin    |         0        |
| Standard output |    stdout   |         1        |
| Standard error  |    stderr   |         2        |

### Redirections
- \> - redirects standard output to a file, **overwriting** existing contents.
- \>> - redirects standard output to a file, **appending** to any existin content.
- < - redirects input from a file to a command.

You can redirect with a file descriptor using `&`:
- `2>&1` - combine stderr and stdout
- `2>file` - redirects stderr to a file

### The Null Device
You can ignore the output by redirecting it to nowhere using:
`/dev/null` using the null device.

# Explorations outside the course

## /dev/random
Any Unix-like OS has /dev/random or something similar such as /dev/random that are special files that serve as pseudorandom number generator.

# Also deployed a Windows Azure VM using Azure CLI
https://cloudacademy.com/lab/deploying-a-windows-azure-vm-using-azure-cli/

