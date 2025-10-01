# ModuleName
pondering path
## Challenge Name
the root
### question
pwn.college{A2gcmzaTLAQTn_zP5l9nlcYtEPD.dhzN5QDL5gDN1czW}

The root was /pwd so by typing that we get the value

```bash
/pwd
BOOM!!!
Here is your flag:
pwn.college{A2gcmzaTLAQTn_zP5l9nlcYtEPD.dhzN5QDL5gDN1czW}
```

### Topics Learnt
after typing the root of the file with / along with the name of the file

### References 
NA


## Challenge Name
Program And Absolute Paths
### question
{AS46hH_bjcXPCh-pbuH6jYHHlpu.dVDN1QDL5gDN1czW}

The Flag as we can see was situated in the absolute path so we can start off by typing the / commands and the the file was in /challenge/run

```bash
/challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{AS46hH_bjcXPCh-pbuH6jYHHlpu.dVDN1QDL5gDN1czW}
```

### Topics Learnt
learned to write absolute path of the files

### References 
NA





## Challenge Name
position thyself
### question
pwn.college{0Iuh__xcUkdPgfmWm53YnxPmLp4.dZDN1QDL5gDN1czW}

got a directory upon running the command and after visiting the path i ran the command

```bash
/cd /proc
hacker@paths~position-thy-self:/proc$ cd 138
hacker@paths~position-thy-self:/proc/138$ cd fd
hacker@paths~position-thy-self:/proc/138/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0Iuh__xcUkdPgfmWm53YnxPmLp4.dZDN1QDL5gDN1czW}
```
### topics learnt
learned to traverse different directories
### References 
NA



## Challenge Name
Position  Elsewhere
### question
pwn.college{I3N0TX0-oOO7sLdXtXXKJyNfI3-.ddDN1QDL5gDN1czW}

got a directory upon running the command and after visiting the path i ran the command

```bash
d /proc
hacker@paths~position-elsewhere:/proc$ cd 138
hacker@paths~position-elsewhere:/proc/138$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{I3N0TX0-oOO7sLdXtXXKJyNfI3-.ddDN1QDL5gDN1czW}
```

### topics learnt
learned to traverse diff directories

### References 
NA



## Challenge Name
Position Yet ElseWhere
### question
pwn.college{wPw1hhXEM2LaSsOtci4ttcw_j6C.dhDN1QDL5gDN1czW}

got a directory upon running the command and after visiting the path i ran the command

```bash
challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{wPw1hhXEM2LaSsOtci4ttcw_j6C.dhDN1QDL5gDN1czW}
```

### topics learnt
learned to traverse different directories

### References 
NA


## Challenge Name
implicit relative path from/
### question
pwn.college{YeJl0tcETuW1aSmxsPvjDNZHmmK.dlDN1QDL5gDN1czW}

used / went to directory then used relative path to the file
```bash
ory
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YeJl0tcETuW1aSmxsPvjDNZHmmK.dlDN1QDL5gDN1czW}
```

### topics learnt
Relative Paths
### References 
NA


## Challenge Name
explicit relative path from/
### question
pwn.college{ggraTwkkPPQLPY4dqrdxAQ6Gfaf.dBTN1QDL5gDN1czW}
used / went to the directory then used ./challenge/run

```bash
/challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ggraTwkkPPQLPY4dqrdxAQ6Gfaf.dBTN1QDL5gDN1czW}
```

### topics learnt
learnt alternative ways of writing relative paths 
    /challenge
    /challenge/.
    /challenge/./././././././././
    /./././challenge/././

### References 
NA

## Challenge Name
Implicit Relative Path
### question
pwn.college{w6RqxVB3sktWrOEH_l5NOvdZesn.dFTN1QDL5gDN1czW}

entered driectory of challenge and used ./flag 
```bash
./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{w6RqxVB3sktWrOEH_l5NOvdZesn.dFTN1QDL5gDN1czW}
```

### topics learnt
used ./ to call explicitly
### References 
NA

## Challenge Name
Home Sweet Home
### question
pwn.college{8_o0RhL0eqSsBypu9oDPyBEFOnn.dNzM4QDL5gDN1czW}
```bash
/challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{8_o0RhL0eqSsBypu9oDPyBEFOnn.dNzM4QDL5gDN1czW}
```

### topics learnt
learnt to write name of file with the help of home directory , start w ~home
### References 
NA
