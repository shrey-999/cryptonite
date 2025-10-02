# Module name
data manipulation
## topic name
translating characters

## flag
pwn.college{YJAisOCBlLfRGJn2fPCAZCULy84.01MxEzNxwCN5UzNzEzW}
```bash
/challenge/run | tr '[:upper:][:lower:]' '[:lower:][:upper:]'
```
tr was used to convert lower case to upper case and vice-versa
The solution involved using the tr command to translate characters in a piped data stream
. The /challenge/run command printed the flag with its character casing swapped.
By piping this output into tr with the character classes [:upper:] and [:lower:],
we were able to simultaneously swap all uppercase characters to lowercase and vice-versa, revealing the correct flag.
### topics learnt
tr character classes
charcter translation
piping for data modification

## challenge
deleting characters

### flag
pwn.college{8GabvssivaVTWuHR1NO2lz7rbz4.0FNxEzNxwCN5UzNzEzW}
```bash
/challenge/run |tr -d ^%
```
usage of tr -d to remove one specific/mulitiple char
### topics learnt
deletion of characters w -d cmd

## challenge
deleting newlines

### flag
pwn.college{c10ITlElRNfkvPRetovdxj07ava.0VNxEzNxwCN5UzNzEzW}
```bash
/challenge/run |tr -d "\n"
```
we use "\n" for newline and the tr -d cmd to delete the new line 

### topics learnt
deletion of new lines

## challenge
extracting first lines with head
### flag
pwn.college{MJejkPrZ2KYxiS2L8BboytjzdEV.0lNxEzNxwCN5UzNzEzW}
```bash
/challenge/pwn | sed 7q | /challenge/college
```
To solve the challenge, you can replace head -n 7 with more versatile tools like sed 7q or awk 'NR < 8'. 
These alternatives also filter the first seven lines from the program's output before piping it onward.
This showcases the flexibility of the Linux command line where multiple tools can achieve the same result.

### topics learnt 
sed <N>q to process first N lines
awk 'NR <= N'
execution path

## challenge
extracting specific sections of the text

### flag
pwn.college{oEVfTVJ8ahdLjA_IoP5TnI-8yTk.01NxEzNxwCN5UzNzEzW}

```bash
/challenge/run | cut -d ' ' -f 2 | tr -d '\n'
```
### topics learnt
Line Filtering Versatility, Delimiter Specificity, piping workflows

## challenge 
storing command output
### flag
pwn.college{gJiaJvv-sGtRfdL70_9gJZJGokC.0FM0MDOxwCN5UzNzEzW}
We fixed the sort command, which failed because of a missing space between the -r option and the file path.
This common syntax error highlighted the need for separating command options from their arguments. 
To get the flag, we combined sort with other tools, piping the output to head or tail to isolate the specific line we needed.

### topics learnt
sorting flags numerically,alphabettically,etc




