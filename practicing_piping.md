# Module name
Practicing Piping
## topic name
redirecting output
### flag
pwn.college{8b_kwTok2RqtLf691rZJcXAM-t9.QX0YTN0wCN5UzNzEzW}
redirected PWN to COLLEGE File , cat'd the college file
```bash
echo PWN>COLLEGE
```
### topics learnt
write output of one file into another , redirection
## challenge
redirecting more output
### flagpwn.college{8IT9VT89_fk2Uizc8qnT7me_RpR.QX1YTN0wCN5UzNzEzW}
ran /challenge/run >> /home/hacker/the-flag
then cat /home/hacker/the-flag
### topics learnt
redirect output 
## challenge
redirecting errors
### flag 
pwn.college{UjzSrMLbScBWYYQopDBFzs2UeTJ.QX3YTN0wCN5UzNzEzW}
redirecting error into a file where we use 2> and read with file w cat
```bash
/challenge/run >myflag 2>instructions
cat myflag
```
### topics learned
learnt writing errors and output into various files and reading flags

## challenge 
redirecting input 
### flag 
pwn.college{MC1rnieLm9tRFuJpfN4-G5L3xIS.QXwcTN0wCN5UzNzEzW}
redirected PWN file into input and read "COLLEGE" out of it 
```bash
/challenge/run >PWN
echo COLLEGE>PWN
/challenge/run <PWN
```
### topics learnt
learnt to redirect PWN file content into the input
## challenge
grepping stored results
### flag
pwn.college{I59PwiIoSKyWtgf73TlZE2mY7K9.QX4EDO0wCN5UzNzEzW}
```bash
/challenge/run > /tmp/data.txt
cd /
cd tmp
grep flag data.txt
grep "pwn.college{" data.txt
```
copied components into data.txt then grep pwn.college to get flag
### topics learnt
learnt composition of multiple functions like redirecting and grep
## challenge
grepping live output
### flag
pwn.college{othJCsCyY8bQ0zps05l7cQXPkxA.QX5EDO0wCN5UzNzEzW}
used piping to search output, grep output with piping cmd
```bash
/challenge/run|grep "pwn.college{"
```
### topics learnt
piping can be used to store ouput and grep with '|'

## challenge
grepping errors 
### flag
pwn.college{0X5o1JnOFloT1j6JX6zkvy0GoX8.QX1ATO0wCN5UzNzEzW}
To search a program's error output, you must first merge the standard error stream (2) into the standard output stream (1) using 2>&1. This is necessary because the pipe (|) only sends standard output to the next command. The full command /challenge/run 2>&1 | grep "pwn.college{" therefore allows grep to filter the error messages for the flag.
```bash
/challenge/run 2>&1|grep "pwn.college{"
```
### topics learnt
filesystem navigation , File I/O Redirection, Searchign and pattern matching

## challenge
filtering with grep -v
### flag
pwn.college{UilbT-FGz3fTdBvYbDnHovi63bD.0FOxEzNxwCN5UzNzEzW}
```bash
/challenge/run|grep -v "DECOY"
```
To find the flag, you use the grep -v command, which inverts the search to show only the lines that do not match a pattern. By piping the program's output to grep -v "DECOY", you filter out all the decoy lines. This isolates the single unique line which is the correct flag.
### topics learnt
inverting searches,advanced filtering

## challenge
duplicating piped data with tee
### flag
pwn.college{U87JAUvMNNbk-b9RRtAIc6YxTec.QXxITO0wCN5UzNzEzW}
```bash
/challenge/pwn | tee output.txt | /challenge/college
cat output.txt
/challenge/pwn --secret "U87JAUvM" | /challenge/college
```
This debugging process used the tee command to intercept data flowing between two commands. By piping the output of /challenge/pwn into tee, we were able to save the output to a file (output.txt) while simultaneously passing it to /challenge/college. This allowed us to discover the secret code required to make the second command work.
### topics learnt
debugging with tee, pipe operator (|)
, duplicating data of a pipeline with tee command

## challenge 
process substitution for input 
### flag
pwn.college{QlfYA6giAp0SWg5rjdmqNUrA3pe.0lNwMDOxwCN5UzNzEzW}
```bash
diff <(/challenge/print_decoys_and_flag) <(/challenge/print_decoys)
```
This command uses process substitution to treat the output of two different commands as if they were temporary files. This is a common and efficient way to compare the output of two commands without having to manually save them to disk. The diff command then shows you the single line that exists in the first output but not in the second, which reveals the flag.
## topics learnt
process substitution, diff cmd, decoys,efficiency

## challenge
writing to multiple programs
### flag
pwn.college{orfz1ZHfW950A71WBsv-508UbPC.QXwgDN1wCN5UzNzEzW}
```bash
/challenge/hack | tee >(/challenge/the) | /challenge/planet
```
The solution involved using a combination of the tee command and process substitution to duplicate a command's output. The output of /challenge/hack was piped to tee, which then simultaneously sent the data to both /challenge/the and /challenge/planet. This method allowed for efficient data duplication to multiple commands without creating intermediate files.

### topics learnt
Process substitution for writing,Piping to multiple commands,The tee commands versatility,Piping vs. process substitution

## challenge
split piping stderr and stdout
### flag
pwn.college{c0N3htuMQuHkPDX4mU61-1EfVUx.QXxQDM2wCN5UzNzEzW}
```bash
/challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
```
learnt a redirection technique that experts struggle with,
The solution used a combination of I/O redirection and process substitution to separate and redirect a command's output. By using > to redirect stdout and 2> to redirect stderr, each output stream from /challenge/hack was sent to its own destination: /challenge/planet and /challenge/the, respectively. This allowed for the independent processing of standard and error outputs without mixing them.
## topics learnt 
redirecting stderr, separating output streams, multiple redirections, advanced substituiton

## challenge
named pipes
### flag
pwn.college{Yq_iMaeNSn3bmv2IttJ_zsycpBB.01MzMDOxwCN5UzNzEzW}
we're supposed to open 2 terminals where we use two separate set of commands
terminal 1:
```bash
cd /
cd tmp
mkfifo flag_fifo
```
terminal 2:
```bash
/challenge/run >/tmp/flag_fifo
cat falg_fifo
```
The solution to the FIFO challenge required using two separate terminals to handle the pipe's blocking behavior. In the first terminal, you create the named pipe (mkfifo) and then run a command to read from it (cat), which will block until a writer connects. In a second terminal, you run the command (/challenge/run) to write its output to the FIFO, which unblocks the first process and allows the data to be read and displayed.

### topics learnt
fifo blocking, persistent named pipes, multi terminal workflow , memory based data transfer
















