# Linux Day 4
## Deleting files
rm file - remove file  
rm -r dir - remove directory and its content  
rm -f file - force removal  

## Copying files
cp source_file destination_file  
cp file1 file2 ... destination_dir - you can copy series of files  
cp -i - run interactive mode   
cp -r source_dir destination  

## Moving and renaming files
mv - Move or rename files and directories  
mv source destination  
m -i source destination  

## Sorting data
sort - sorts text alphabetically in the file  
sort file 
-k F - sort by key; F is the field number  
-r - sort in reverse  
-u - sort unique  

## Creating a collection of files or archives
You can bundle a collection of files with tar.
Create, extract, list contents of a tar archive.
tar. No need for hyphen to use tar options.

c - create a tar archive  
x - extract files from the archive  
t - display the table  
v - be verbose  
z - use compression  
f file - use this file  

## Compressing Files
gzip - compress files  
gunzip - uncompress files  
gzcat - concatenates compressed files  
zcat - concatenates compressed files  

du - estimates file usage  
du -k - displays in kilobytes  
du -h - displays in human readble format  

You can compress tars witgh gzip.  