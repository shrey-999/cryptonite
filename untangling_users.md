# Module Name
Untangling_Users

## challenge
Becoming root with su

## flag
pwn.college{M98qzizJk7fPoZWCblRTX1yMUSe.dVTN0UDL5gDN1czW}

First, I used the su command and the provided password to become the root user. The flag was in two parts. I found the first part in the hacker's home directory. For the second part, I had to navigate to the root user's home directory (/root), which I couldn't access before. After searching through some hidden directories, I found the second half of the flag.

```bash

su
hack-the-planet
cat /home/hacker/the-flag
cd /root
cat .cache/pip/http-v2/b/6/0/6/a/b606a6d3a5fafd1fbaff975adcfccc996fcd9d417a8e813d80f89d7a.body
```
### topics learnt
Learned that becoming root gives you access to protected directories like /root. Also learned that the root user has its own separate home directory with its own files.

### Reference 
NA

## challenge
other users with su

### flag
pwn.college{sLd7A4yiEjjd6RCTmVgX3um6Zrm.dZTN0UDL5gDN1czW}

For this one, I had to switch to a different user, zardus, not just root. I provided the username as an argument to the su command, entered the password for zardus, and then ran the challenge binary to get the flag.

```bash

su zardus
dont-hack-me
/challenge/run
```
### topics learnt
Learned that su can be used to become any user on the system, not just the root user, by providing their username.

### reference 
NA

## Challenge 
Cracking passwords

### flag
pwn.college{U_TpDbDptly1Vrx4OGwyWFnamiI.ddTN0UDL5gDN1czW}

This challenge involved a leaked password hash file. I used the password cracking tool john on the /challenge/shadow-leak file. After john cracked the hash, I used the --show command to reveal the password. Then I used that password to su into the zardus account and get the flag.

```bash

john /challenge/shadow-leak
john --show /challenge/shadow-leak
su zardus
aardvark
/challenge/run
```
### topics learnt
Learned how to use a basic password cracker like John the Ripper to find a password from a leaked hash file.

### reference 
NA

## Challenge 
Using sudo

### flag
pwn.college{onPLlA16wy5zsba6q-BiTmZiA-m.dhTN0UDL5gDN1czW}

First, I listed the files and found a flag file that was owned by root. When I tried to cat it, I got a "Permission denied" error. By using sudo before the cat command, I was able to run just that one command with root privileges and read the file to get the flag.

```bash

ls -l
cat not-the-flag
sudo cat not-the-flag
```
### topics learnt
Learned that sudo is used to run a single command with root privileges without needing to switch to a full root shell. It's useful for quick administrative tasks.

### reference
NA
