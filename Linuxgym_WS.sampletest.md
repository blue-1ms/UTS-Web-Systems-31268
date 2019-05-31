# Exam Samples

# Q1 Create Directory
mkdir sample

# Q2 Create File
touch onya.txt

# Q3 List files in a directory
ls /usr/local/linuxgym-data/gutenberg/3* > list_3_files

# Q4 myper.txt
touch myperm.txt
chmod 611 myperm.txt

# Q5 Create bash
vim hello.sh

code:
#!/bin/bash
echo Hello $@ 
:wq

chmod 711 hello.sh

# Q6 Count words
wc - w /usr/local/linuxgym-data/gutenberg/0ws0310.txt > count.out
vim count.out delete the file path

# Q7 First 1000 Lines
head -n1000 /usr/local/linuxgym-data/gutenberg/0ws0310.txt > top.txt
vim top.txt
:%s/Queene/Queen
:wq

