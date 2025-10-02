# ModuleName
pondering path
## Challenge Name
the root
### question
pwn.college{g7mfOELVrSGz_dNjb0FKw6zpUTk.QX4cTO0wCN5UzNzEzW}
The root was /pwd so by typing that we get the value

```bash
/pwd
BOOM!!!
Here is your flag:
pwn.college{g7mfOELVrSGz_dNjb0FKw6zpUTk.QX4cTO0wCN5UzNzEzW}
```

### Topics Learnt
after typing the root of the file with / along with the name of the file

### References 
NA


## Challenge Name
Program And Absolute Paths
### question
pwn.college{Iw6BNa_9qEXiFSdh-wsxJaUzdoD.QX1QTN0wCN5UzNzEzW}

The Flag as we can see was situated in the absolute path so we can start off by typing the / commands and the the file was in /challenge/run

```bash
/challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{Iw6BNa_9qEXiFSdh-wsxJaUzdoD.QX1QTN0wCN5UzNzEzW}
```

### Topics Learnt
learned to write absolute path of the files

### References 
NA





## Challenge Name
position thyself
### question
pwn.college{ElDbenj9jovQsIFvd9hkPd0akjt.QX2QTN0wCN5UzNzEzW}
got a directory upon running the command and after visiting the path i ran the command

```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/doc/fontconfig
hacker@paths~position-thy-self:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{ElDbenj9jovQsIFvd9hkPd0akjt.QX2QTN0wCN5UzNzEzW}
```
### topics learnt
learned to traverse different directories
### References 
NA



## Challenge Name
Position  Elsewhere
### question
pwn.college{UNt6C3sfqnac4XMhKD14VX7YmWO.QX3QTN0wCN5UzNzEzW}

got a directory upon running the command and after visiting the path i ran the command

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /home directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /home
hacker@paths~position-elsewhere:/home$ ~$ /home
-bash: ~$: command not found
hacker@paths~position-elsewhere:/home$ challenge/run
-bash: challenge/run: No such file or directory
hacker@paths~position-elsewhere:/home$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{UNt6C3sfqnac4XMhKD14VX7YmWO.QX3QTN0wCN5UzNzEzW}
```

### topics learnt
learned to traverse diff directories

### References 
NA



## Challenge Name
Position Yet ElseWhere
### question
pwn.college{4Jw86Imc3qykpRloLY9JUfgbSFD.QX4QTN0wCN5UzNzEzW}


got a directory upon running the command and after visiting the path i ran the command

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/include
hacker@paths~position-yet-elsewhere:/usr/include$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4Jw86Imc3qykpRloLY9JUfgbSFD.QX4QTN0wCN5UzNzEzW}
```


### topics learnt
learned to traverse different directories

### References 
NA


## Challenge Name
implicit relative path from/
### question
pwn.college{IkBY7VbbmgQh5lCzUsoQiAqbnQM.QX5QTN0wCN5UzNzEzW}

used / went to directory then used relative path to the file
```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~implicit-relative-paths-from-:/$ cd /c
-bash: cd: /c: No such file or directory
hacker@paths~implicit-relative-paths-from-:/$ cd //c
-bash: cd: //c: No such file or directory
hacker@paths~implicit-relative-paths-from-:/$ c
-bash: c: command not found
hacker@paths~implicit-relative-paths-from-:/$ /c
-bash: /c: No such file or directory
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IkBY7VbbmgQh5lCzUsoQiAqbnQM.QX5QTN0wCN5UzNzEzW}
hacker@paths~implicit-relative-paths-from-:/$ 
```

### topics learnt
Relative Paths
### References 
NA


## Challenge Name
explicit relative path from/
### question
pwn.college{MLicXTVzGDUgbsOc-QD50P0KsFY.QXwUTN0wCN5UzNzEzW}
used / went to the directory then used ./challenge/run

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ .
-bash: .: filename argument required
.: usage: . filename [arguments]
hacker@paths~explicit-relative-paths-from-:/$ .challenge/run
-bash: .challenge/run: No such file or directory
hacker@paths~explicit-relative-paths-from-:/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~explicit-relative-paths-from-:/$ /challenge/.run
-bash: /challenge/.run: No such file or directory
hacker@paths~explicit-relative-paths-from-:/$ cd/challenge
-bash: cd/challenge: No such file or directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MLicXTVzGDUgbsOc-QD50P0KsFY.QXwUTN0wCN5UzNzEzW}
hacker@paths~explicit-relative-paths-from-:/$ 


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
pwn.college{gUznquOjbQRKoEXgqER7nv7plSw.QXxUTN0wCN5UzNzEzW}

entered directory of challenge and used ./flag 
```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gUznquOjbQRKoEXgqER7nv7plSw.QXxUTN0wCN5UzNzEzW}

```

### topics learnt
used ./ to call explicitly
### References 
NA

## Challenge Name
Home Sweet Home
### question
pwn.college{86Blh3ukAabrXWwMblNcdx7doyO.QXzMDO0wCN5UzNzEzW}
```bash
hacker@paths~home-sweet-home:~$ /challenge/run
You must provide an argument to /challenge/run when you invoke it!
hacker@paths~home-sweet-home:~$ /challenge/run~/a
-bash: /challenge/run~/a: No such file or directory
hacker@paths~home-sweet-home:~$ cd challenge
-bash: cd: challenge: No such file or directory
hacker@paths~home-sweet-home:~$ cd /
hacker@paths~home-sweet-home:/$ challenge/run~/a
-bash: challenge/run~/a: No such file or directory
hacker@paths~home-sweet-home:/$ /challenge/run~/a
-bash: /challenge/run~/a: No such file or directory
hacker@paths~home-sweet-home:/$ ^C
hacker@paths~home-sweet-home:/$ /challenge/run ~/ae
The argument you provided must not have been longer than 3 characters (it's 
currently 4 characters long)!
hacker@paths~home-sweet-home:/$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{86Blh3ukAabrXWwMblNcdx7doyO.QXzMDO0wCN5UzNzEzW}
hacker@paths~home-sweet-home:/$ ^C
hacker@paths~home-sweet-home:/$
```



### topics learnt
learnt to write name of file with the help of home directory , start w ~home
### References 
NA
