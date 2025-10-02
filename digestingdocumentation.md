# ModuleName
Digesting documentation
## challenge
learning from documentation
### question
pwn.college{gDoRIkDGicsNl01Gt5X8OZbRuSf.QX0ITO0wCN5UzNzEzW}
```bash
/challenge/challenge --giveflag
```
### topics learnt
passing arugment with command
## challenge
learning complex usage
### question/flag
pwn.college{YlE8UB4ULvQ01y3a_Saj-U0R5mY.QX1ITO0wCN5UzNzEzW}
we use argument printfile , first we use command/ challenge/challenge then arugment with name of required file 
```bash
/challenge/challenge --printfile /flag
```
### topics learnt
usage of argument to find syntax from doc
## challenge name
reading manuals
### flag
pwn.college{sJIG-UeywE15Pd5qPv6a7ILGc-J.QX0EDO0wCN5UzNzEzW}
first ran man, then got the further hints/details from there
```bash
man challenge
/challenge/challenge -- seywdq 155
```
## topics learnt
learnt reading docs w man cmd
## challenge
searching manuals
### flag
typed man challenge went to man doc typed flag got parameter 
```bash
man challenge
/challenge/challenge --
```
### topics learnt 
traverse through manual
## challenge
searching for manuals
### flag
pwn.college{QuBKqKALZsqmSAumPX2lBUXqOLP.QX2EDO0wCN5UzNzEzW}
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
uqsqmumlqw (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man uqsqmumlqw
hacker@man~searching-for-manuals:~$ /challenge/challenge --uqsqmu 220
Correct usage! Your flag: pwn.college{QuBKqKALZsqmSAumPX2lBUXqOLP.QX2EDO0wCN5UzNzEzW}
```
### topics learnt
using manual to get required syntaxes of man , etc
## challenge name
helpful programs
### flag
pwn.college{EdrkvwCx8y-XOB6g5X9phVU5MUs.QX3IDO0wCN5UzNzEzW}
```bash
hacker@man~helpful-programs:~$ /challenge/run --help
-bash: /challenge/run: No such file or directory
hacker@man~helpful-programs:~$ /challenge/run --help
-bash: /challenge/run: No such file or directory
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give
                        you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 865
hacker@man~helpful-programs:~$ /challenge/challenge --865
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: unrecognized arguments: --865
hacker@man~helpful-programs:~$ /challenge/challenge -g 865
Correct usage! Your flag: pwn.college{EdrkvwCx8y-XOB6g5X9phVU5MUs.QX3IDO0wCN5UzNzEzW}
```
### topics learnt
learnt usage of help instead of man
## challenge
help for builtins
### flag
pwn.college{w2ocPLD5CE-wSAoP22bArDKlRog.QX0ETO0wCN5UzNzEzW}
help challenge then followed further instructions
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "w2ocPLD5".
hacker@man~help-for-builtins:~$ challenge --secret w2ocPLD5
Correct! Here is your flag!
pwn.college{w2ocPLD5CE-wSAoP22bArDKlRog.QX0ETO0wCN5UzNzEzW}
```
### topics learnt 
using builtin funcitons
