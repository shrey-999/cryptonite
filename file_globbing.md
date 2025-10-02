# Module name
file globbing
## topic name
Matching with *
### flag
pwn.college{Ye0xM7kRVvW5k72Gffv6iWP-K10.QXxIDO0wCN5UzNzEzW}
read instructions went to directory ran command
```bash
cd /ch*
/challenge/run
```
usage: 
```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Ye0xM7kRVvW5k72Gffv6iWP-K10.QXxIDO0wCN5UzNzEzW}
```
### topics learnt 
matching trailing values
## challenge
matching with ?
### flag
pwn.college{c1WqgsfBgWty2UWPpCoXxQ7gnmm.QXyIDO0wCN5UzNzEzW}
because ? matched with one character wrote cd , replaced ,went to the directory
usage:
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{c1WqgsfBgWty2UWPpCoXxQ7gnmm.QXyIDO0wCN5UzNzEzW}
hacker@globbing~matching-with-:/challenge$ ^C
```
### topics learnt
learnt matching characters ?
## challenge 
matching with []
### flag
pwn.college{ElJxhmhBXhZ0BB3RUvIuBrtA4c2.QXzIDO0wCN5UzNzEzW}
[] is used to set the parameters so we put paramters of flag in direc
### topics learnt
usage of [] for matching arguments
## challenge
matching paths with []
### flag
pwn.college{AHVCsT9A1UVqzYJCd5OX7LH7c6h.QX0IDO0wCN5UzNzEzW}
used challenge/run then searched for patterns with bash and wrote in square brackets
### topics learnt 
matching paths with [] from home dir
## challenge
multiple globs
pwn.college{IcQETQFBB0B7jLkIeVghI2kS8on.0lM3kjNxwCN5UzNzEzW}
visited dir then challenge/run with 3 char p
```bash
cd /challenge/files
/challenge/run *p*
```
### topics learnt
usage of multiple astrix '*' to match name
## challenge
mixing globs
### flag
pwn.college{onLy9dPiYt4G6wRU3kmaSGyMruO.QX1IDO0wCN5UzNzEzW}
To match a 6-character word starting with 'c', 'e', or 'p', use the glob pattern [cep]?????. The [cep] part matches the first required letter,
while each ? matches a single character, enforcing the exact length of the remaining five. This is more precise than using *,
which would incorrectly match words of any length.
```bash
cd /challenge/files
/challenge/run [cep]*
```
### topics learnt
usage of mix globes to match file names
## challenge
exclusionary globbing
### flag
pwn.college{gKf5PRrWc7NEDqV9UsWPtT-dmsl.QX2IDO0wCN5UzNzEzW}
```bash
cd /challenge/files
/challenge/run [!pwn]*
```
To exclude characters in a glob, use an exclamation mark ! as the first character inside the brackets [ ].
For example, the pattern [!pwn]* matches any file that does not start with the letters 'p', 'w', or 'n'. The ! inverts the set
, filtering out any names that begin with those characters.

### topics learnt
usage of glob
## challenge
tab completion
### flag
pwn.college{8I26riluDeyZa6NjmHXQC-5-zlz.0FN0EzNxwCN5UzNzEzW}
tab completion works automatically upon typing cat/challenge/pwn, so it catches on to the possibility , sorta like prediction
```bash
cat /challenge/pwn
```
then press tab
### topics learnt
using tab for autocompletion
## challenge
mutliple options for tab completion
### flag
pwn.college{EIG_Kc-exkcZf0w-iADDweJySo-.0lN0EzNxwCN5UzNzEzW}
went to cd challenge files , typed in cat and pressed tab resulted in multiple paths, after cat'ing some of them i got the flag in pwn collge flag
```bash
cd /challenge/files
cat p<tab>
cat pwn<tab>
cat pwncollege-flag
```
### topics learnt
using tab function multiple times to find the flag path
## challenge 
tab completion on commands
### flag 
pwn.college{EcFHvKCFB5uCpbiVY2QRLodcegX.0VN0EzNxwCN5UzNzEzW}
just type in pwncollege and press tab , it autocompletes , press enter , it gives us the flag
```bash
pwncollege<tab>
pwncollege-12877
```
### topics learnt
using tab to complete commands



