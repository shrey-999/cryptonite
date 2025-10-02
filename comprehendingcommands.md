# module name
comprehending commands
## Challenge Name
cat:not the pet,but the command!
### Solve
pwn.college{0HycOJSrRmD9_arD3mGIntMDP1K.QX5ETO0wCN5UzNzEzW}
 the flag was found by cat flag
```bash
/pwd
cat flag
```

### New Learnings
learnt to read file using cat 

### References 
NA
## challenge name
catting absolute path
### solve
```hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{0HycOJSrRmD9_arD3mGIntMDP1K.QX5ETO0wCN5UzNzEzW}
hacker@commands~catting-absolute-paths:~$ ^C
```
###  topics learnt 
catting absolute paths
### references 
NA
## Challenge name
more catting practice
## flag
pwn.college{EcpsrpjsX6HbqsaMeyPQJL1Ysyw.QXwITO0wCN5UzNzEzW}

``` hacker@commands~more-catting-practice:~$ cat /usr/share/sounds/flag
pwn.college{EcpsrpjsX6HbqsaMeyPQJL1Ysyw.QXwITO0wCN5UzNzEzW}
```
## topics learnt 
cat w out changing directory
### references 
NA
## challenge
grepping for a needle in a haystack
### question
pwn.college{Ah4JpO-zm9pELXlyX41TSBjg2vd.QX3EDO0wCN5UzNzEzW}
 find the file with the name of pwn.college with help of grep 

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{Ah4JpO-zm9pELXlyX41TSBjg2vd.QX3EDO0wCN5UzNzEzW}

```

### topics learnt
learnt to extract the words from a large file with grep

### References 
NA
## challenge
comparing files
### question
pwn.college{Au_z6R1KQYhsmYazSMzzjXl4rPB.01MwMDOxwCN5UzNzEzW}

 
visited the challenger directory and then diff between two file given

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
16a17
> pwn.college{Au_z6R1KQYhsmYazSMzzjXl4rPB.01MwMDOxwCN5UzNzEzW}
hacker@commands~comparing-files:~$ ^C

```

### topics learnt
we learn to find the difference between two files 
### References 
NA
## challenge
Listing files
### question
pwn.college{Y69RCwyRzdPaHDhNka9JnTxx7_Y.QX4IDO0wCN5UzNzEzW}


went to the directory listed the file found the new name and ran that with /challenge to find the flag

```bash
ls
/challenge/23666-renamed-run-19284
```

### topics learnt
learnt listing the files in a directory

### References 
NA
## challenge
Touching Files
### question
pwn.college{Mu1Dhe4CB0w_g43taYzBzvOqIFZ.QXwMDO0wCN5UzNzEzW}


touched and created two files then ran challenge

```bash
touch /tmp/pwn
touch /tmp/college
```

### topics learnt
learned to create using touch 

### References 
NA
## challenge
removing files
### question
pwn.college{cc2ulEJxQY23ZL7BW_By73rXb1d.QX2kDM1wCN5UzNzEzW}

used the rm to delete  file, the root directory then used command for check
```bash
rm delete_me
/challenge/check
```

### topics learnt
removal of a file from directory

### References 
NA
## challenge
Moving Files
### question
pwn.college{YLBij2X89FTAO9URdnSMphZkarS.0VOxEzNxwCN5UzNzEzW}
 needed to move file so went to / directory , write mv to move to next file
```bash
cd /
mv flag tmp/hack-the-planet
```

### topics learnt
learnt to move from files of different directories and the content too

### References 
NA
## challenge
hidden files
### question
pwn.college{4z0_vn3TcuYUR-ZB1t0tvItldYD.QXwUDO0wCN5UzNzEzW} 

visited directory , typed dis ls -a and found all of the flags
```bash
cd /
ls -a
```

### topics learnt
learnt to list hidden flag of a directory

### References 
NA

## Challenge
an epic filesystem quest
## question
pwn.college{0fS23hzx9qJ0rCEs7z7tDdmcAS3.QX5IDO0wCN5UzNzEzW}
first removed the file present then created the symlink then cat with the given command
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
WHISPER  challenge  flag  lib32   media  opt   run   sys  var
bin      dev        home  lib64   mnt    proc  sbin  tmp
boot     etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat WHISPER
Congratulations, you found the clue!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl5

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/x86_64-linux-gnu/perl5
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ ls
5.30  TEASER
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ cd TEASER
-bash: cd: TEASER: Not a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ cat TEASER
Yahaha, you found me!
The next clue is in: /usr/share/gap/pkg/SmallGrp/doc

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ ls /usr/share/gap/pkg/SmallGrp/doc
BRIEF-TRAPPED    chapBib.html     manual.css         ragged.css
SmallGrp.toc.gz  chapBib.txt      manual.js          rainbow.js
chap0.html       chapBib_mj.html  manual.pdf         times.css
chap0.txt        chapInd.html     manual.six.gz      toggless.css
chap0_mj.html    chapInd.txt      manualbib.xml      toggless.js
chap1.html       chapInd_mj.html  manualbib.xml.bib
chap1.txt        chooser.html     mathjax
chap1_mj.html    lefttoc.css      nocolorprompt.css
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ cat /usr/share/gap/pkg/SmallGrp/doc/BRIEF-TRAPPED
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/drivers/misc/eeprom

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ ls -a /opt/linux/linux-5.4/drivers/misc/eeprom
.                Kconfig   built-in.a          eeprom_93cx6.c
..               Makefile  digsy_mtc_eeprom.c  eeprom_93xx46.c
.README          at24.c    ee1004.c            idt_89hpesx.c
.built-in.a.cmd  at25.c    eeprom.c            max6875.c
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ cat /opt/linux/linux-5.4/drivers/misc/eeprom/.README
Tubular find!
The next clue is in: /usr/lib/x86_64-linux-gnu/gedit/plugins/quickopen/__pycache__

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5$ cd /usr/lib/x86_64-linux-gnu/gedit/plugins/quickopen/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gedit/plugins/quickopen/__pycache__$ ls
NOTE  __init__.cpython-38.pyc  popup.cpython-38.pyc  virtualdirs.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gedit/plugins/quickopen/__pycache__$ cat flag
cat: flag: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gedit/plugins/quickopen/__pycache__$ cat NOTE
Lucky listing!
The next clue is in: /usr/lib/ruby/gems/2.7.0/gems/reline-0.1.2
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gedit/plugins/quickopen/__pycache__$ cd /usr/lib/ruby/gems/2.7.0/gems/reline-0.1.2
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/gems/2.7.0/gems/reline-0.1.2$ ls
LEAD
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/gems/2.7.0/gems/reline-0.1.2$ cat LEAD
Tubular find!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/udhcpc/default
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/gems/2.7.0/gems/reline-0.1.2$ cat /opt/busybox/busybox-1.33.2/include/config/udhcpc/default
cat: /opt/busybox/busybox-1.33.2/include/config/udhcpc/default: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/gems/2.7.0/gems/reline-0.1.2$ cd /opt/busybox/busybox-1.33.2/include/config/udhcpc/default
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/udhcpc/default$ ls 
POINTER  script.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/udhcpc/default$ cat POINTER
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/udhcpc/default$ cd /usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__$ ls -a
.                                test_masked_matrix.cpython-38.pyc
..                               test_matrix_linalg.cpython-38.pyc
.MEMO                            test_multiarray.cpython-38.pyc
__init__.cpython-38.pyc          test_numeric.cpython-38.pyc
test_defmatrix.cpython-38.pyc    test_regression.cpython-38.pyc
test_interaction.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__$ cat .MEMO
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/racket-doc/scribblings/getting-started/compiled

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__$ ls /usr/share/racket/pkgs/racket-doc/scribblings/getting-started/compiled
CUE-TRAPPED                getting-started_scrbl.zo  info_rkt.zo
getting-started_scrbl.dep  info_rkt.dep
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__$ cat /usr/share/racket/pkgs/racket-doc/scribblings/getting-started/compiled/CUE-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{0fS23hzx9qJ0rCEs7z7tDdmcAS3.QX5IDO0wCN5UzNzEzW}
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__$ ^C
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/matrixlib/tests/__pycache__$
```
## topics learnt
learnt various commands their use, used ls cd cat
## references 
NA
## Challenge
Making Directories
## flag
pwn.college{gUwbF6nTUxZZLMVUCwm98qUuE1D.QXxMDO0wCN5UzNzEzW}
```bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{gUwbF6nTUxZZLMVUCwm98qUuE1D.QXxMDO0wCN5UzNzEzW}
```
## topics learnt
making a new directory
## challenge
finding files
## flag
used find main cmdd got multiple files, cat in one of em and got flag
```bash
find /flag/home/hacker
cat f
```

### topics learnt
learnt to find a particualr name from the list of files

### References 
NA













      
