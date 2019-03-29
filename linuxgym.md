[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2F1MSEZ%2FRandom.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2F1MSEZ%2FRandom?ref=badge_shield)

# CH2
ch2 insert
mkdir ch2-vim
Cd mkdir ch2-vim
vim hw.txt
i
hello world
Esc
:wq

ch2 join lines
cp /usr/local/linuxgym-data/vimdata/wordlist.txt wordlist.txt
vim wordlist.txt

ch2 delete a word 
cp /usr/local/linuxgym-data/teeny/1mwsm10.txt 1mwsm10.txt
6G
esc i
dw
:wq

ch2 search and delete
cp /usr/local/linuxgym-data/gutenberg/07frd10.txt 07frd10.txt
vim 07frd10.txt
: /opera-girls
dd
:wq

ch2 delete by line numbers
cp /usr/local/linuxgym-data/gutenberg/0ws3110.txt 0ws3110.txt
vim 0ws3110.txt
G50
4000dd
:wq

ch2 copy and paste line
10yy
OR
10dd
GP

ch2 delete end file 
G1024
(large number)dd

ch2 search and replace
:%s/and/OR/gc

ch2 cut and paste by markers
yy – copy
dd- copy & delete
P – paste

mw d'w p

# CH3
ch3 whoami
whoami > myuserid

ch3 perm to read
chmod +/- user(u) group(g) o(others) read(r) w(write) x(execute)

ch3 error message
cat > stderr.out
cat forgotten.txt 2> stderr.out


# CH5
ch5 count.txt
wc -w /usr/local/linuxgym-data/gutenberg/0ws0310.txt > count.txt

ch5 pipecount.txt
cat | wc –m
type a few lines
ctrl d
cat /usr/local/linuxgym-data/gutenberg/0ws0310.txt | wc –m > pipecount.txt

ch5 wsfiles.txt
touch wsfiles.txt
cd /usr/local/linuxgym-data/emptystuff/
*ws* > ~ch5/pipewild/wsfiles.txt
ls *ws* > /home/student/ch5-pipewild/wsfiles.txt

ch5 s2 directory
cp *s2* /usr/local/linuxgym-data/gutenberg

ch5 copy directory
cp –r /usr/local/linuxgym-data/teeny teeny

ch5 large_to_small
touch large_to_small
cd /usr/local/linuxgym-data/gutenberg
ls –S > ~/ch5-pipewild/large_to_small

# CH6
ch6 print.sh
#!/bin/bash
echo Hello World

ch6 arg.sh
#!/bin/bash
echo $2

ch6 args.sh
#!/bin/bash
echo $@

ch6 add.sh
#!/bin/bash
sd=17
sum= $(( $1 + $sd))
echo $sum

ch6 numargs.sh
#!/bin/bash
echo $#

ch6 stderr.sh
#!/bin/bash
echo $* 1>&2

ch6 lsstderr.sh
#!/bin/bash
ls $1 > &2

ch6 wcscript.sh
#!/bin/bash
cat $1 | wc –w

ch6 checknumargs.sh
#!/bin/bash
if [ $# != 3 ]
then
echo error 1>&2
else
echo $*
fi

# CH7

ch705
grep -l "Anne" /usr/local/linuxgym-data/gutenberg/* > anne-files.txtss

ch706
grep -w "Anne" /usr/local/linuxgym-data/gutenberg/12frd10.txt > anne-words.txt

ch707
grep ^[MN]AT /usr/local/linuxgym-data/census/femalenames.txt > natmat.txt

ch708
#!/bin/bash
grep -w $1 ./table.csv | cut -f2 -d,

ch709
#!/bin/bash
grep -q $1 ./table.csv
if [ $? = 0 ]
then
echo female
else
echo male
fi

ch710
#!/bin/bash
a=`grep -w $1 ./table.csv | cut -f2 -d,`
grep -w $a ./table.csv | cut -f1 -d, | sort
