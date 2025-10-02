# Module name
shell variables
## topic name
printing variables
### flag
pwn.college{UKb3QuICIC6gxPyj7c73ve-2oGd.QX3UTN0wCN5UzNzEzW}
echo shows the content of var by using $
```bash
echo $FLAG
```
### topics learnt
echoing variables using $

## challenge
setting variables
### flag
pwn.college{sgz5VnR2ELcHgVWgZSuQZckEORm.QX5UTN0wCN5UzNzEzW}
commands used:
```bash
PWN=COLLEGE
```
sets variable with value , $PWN is set to access variable
### topics learnt 
variables are case sensitive, learnt to set variable

## challenge 
multi-word variables
### flag
pwn.college{kvhIDSGFhJWLv6yB5O13cp7h0tP.QXwYTN0wCN5UzNzEzW}
```bash
PWN="COLLEGE YEAH"
```
learned to set PWN Variable as "COLLEGE YEAH"
### topics learnt
learnt to multiple words in a var with quotes

## challenge 
exporting variables
### flag
pwn.college{89aQsj9An7O_6pJ5JZ64bpetInV.QXyYTN0wCN5UzNzEzW}
```bash
export PWN=COLLEGE
COLLEGE=PWN
/challenge/run $PWN
```
we're told to export pwn but not college, so exported pwn then ran challenge/run cmd using accessor

### topics learnt
exporting var , and multiple ways to access them

## challenge 
printing exported variables
### flag
pwn.college{gKh4s_WMXTjy4Mo14JhuO1KPvQ-.QX4UTN0wCN5UzNzEzW}
used env to get the output , and using env grep flag we found the flag
```bash
env
env | grep FLAG
```
### topics learnt 
using env, storing cmd output

## challenge
Storing Command Output
### flag
pwn.college{U_B_6LVQXvpHYb_thWMcCPvNveu.QX1cDN1wCN5UzNzEzW}

```bash
PWN=$(/challenge/run)
cat $PWN
```
was told to store output of challenge/run in a var, stored output in dir , then catted file with $

### topics learnt
content of command storing in var

## challenge 
reading input 

### flag
pwn.college{M3nEfbJbz4hkTN2AQTaYmn3Ukyr.QX4cTN0wCN5UzNzEzW}

```bash
read PWN
COLLEGE
```

### topics learnt
read and store user val in var

## challenge
reading files

### flag
pwn.college{YYfpFboXNwifbdjzjZtm_51Snjl.QXwIDO0wCN5UzNzEzW}

```bash
read PWN </challenge/read_me
```
 ### topics learnt 
 read and feed input into another file and read it again
 


