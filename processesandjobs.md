# Module name
processes and jobs
## challenge 
Listing processes
### flag
pwn.college{Q3gcNfwOsjTLCcxRLkNLWbJ8RK_.QX4MDO0wCN5UzNzEzW}
```bash
ps auxww | grep /challenge
/challenge/16131-run-6370
```
We found a hidden program by listing all system processes and filtering the output. 
Using ps auxww generated a complete list of running commands,
which we then piped to grep /challenge to isolate the target process.
This allowed us to discover the full, randomized executable path needed to complete the challenge.

### topics learnt
showing running processes , process listing , discovery without ls , wide output, grep finding itself

## challenge 
killing processes 

### flag
pwn.college{omgbjNrOoF8X7duAziMobwgg3vp.QXyQDO0wCN5UzNzEzW}
```bash
 ps  -ef|grep dont_run
kill 136
/challenge/run
```
after we kill/terminate the process we get the flag
### topics learnt 
killing processes and pid

##challenge 
interrupting processes
### flag
pwn.college{09VqfRMoEaaOTiJ0xqCqZnq9gX1.QXzQDO0wCN5UzNzEzW}
ran /challenge/run and by bruteforcing/interrupting by pressing ctrl+c we get the flag
```bash
/challenge/run
ctrl^c
```
### topics learnt
bruteforcing/interrupting

## challenge
killing misbehaving processes
### flag
pwn.college{8_eXfASgm6CsERrHsxR7yg6_VIw.0FNzMDOxwCN5UzNzEzW}
```bash
ps aux | grep decoy
kill 143
cat /tmp/flag_fifo &
/challenge/run
```
The challenge required stopping a decoy process that was blocking a named pipe by spamming it with fake flags.
We used ps and grep to find the decoy's Process ID (PID) and then terminated it with the kill command. 
Once the pipe was clear, running the main program allowed the real flag to be successfully received.
### topics learnt 
backgrounding with &, dealing with misbehaving processes

## challenge
suspending processes

### flag
pwn.college{IbkwZh2qO4FuWSeJ3_hAIq3eQwP.QX1QDO0wCN5UzNzEzW}

```bash
/challenge/run
/challenge/run
```
used ctrl z to make another version/copy run in the terminal

### topics learnt 
using ctrl z to run another copy in background

## challenge 
resuming processes

### flag
pwn.college{Eur-L5Y2ArskRtHxkxcWSkVpk4L.QX2QDO0wCN5UzNzEzW}

```bash
/challenge/run
ctrl^z
fg
```
learnt to resume suspended commands, ctrl z is used to pause the program and fg to resume it 

### topics learnt 
resume suspended programs using fg , ctrl z to pause

## challenge 
backgrounding processes

### flags
pwn.college{Ut1JT4HKApsiIRlliDF41dCD_cH.QX3QDO0wCN5UzNzEzW}

```bash
/challenge/run
ctrl^z
bg
/challenge/run
```
used challenge to let process run , let it suspend , bg to run it in the background then challenge again to get the flag

### topics learnt 
bg is used to run processes in the background

## challenge 
foregrounding processes
### flag
pwn.college{kL5rLOlxIo4RdeESiV8QvVzzr86.QX4QDO0wCN5UzNzEzW}

```bash
/challenge/run
ctrl^z
bg
fg
```
we suspended the process, it was sent to the background

### topics learnt 
foregrounding of a process suspended in the background , usage of fg bg commands

## challenge 
starting background processes 
### flag
pwn.college{Iz8lF8JhkOy11089ryE2oI1MkPs.QX5QDO0wCN5UzNzEzW}

```bash
/challenge/run &
```
This command executes the /challenge/run program in the background. 
The ampersand (&) symbol tells the shell not to wait for the program to finish.
This frees up your terminal immediately, allowing you to run other commands while the program continues its work independently.
### topics learnt 
ampersand(&), non blocking execution

## challenge 
process exit codes

### flag
pwn.college{QzjjMVmQQzoFH6_pp1bDJM-tyIC.QX5YDO1wCN5UzNzEzW}

```bash
/challenge/get-code
echo $?
/challenge/submit-code 20
```
This sequence first runs a program, /challenge/get-code, which exits with a hidden numerical status. 
The second command, echo $?, reveals this hidden number by printing the exit code of the last command that ran.
Finally, that discovered number is passed as a command-line argument to /challenge/submit-code to solve the challenge.
### topics learnt 
exit codes , $? variable , command line arguments









