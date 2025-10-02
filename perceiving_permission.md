# Module name
perceiving permission
## challenge
Changing file ownership

### flag
pwn.college{ICZYQMaTLEzq4XWRv1-CSrtowha.dFTM2QDL5gDN1czW}

First, I checked the permissions on /flag and saw it was owned by root. I couldn't read it. I used the chown command to change the owner of the file to my current user, hacker. After I owned the file, I was able to read it with cat.

```bash

ls -l /flag
chown hacker /flag
cat /flag
```
### topics learnt
Learned how to use chown to change a file's owner. This lets you access files you couldn't before if you make yourself the new owner.

### Reference 
NA

## challenge
Groups and files

### flag
pwn.college{sZ-WpkHg9y4K2zCJhF-lZgZCg7H.dFzNyUDL5gDN1czW}

This time, instead of changing the owner, I just changed the group. I used chgrp to change the group of /flag to hacker. Since my user is part of the hacker group, this gave me permission to read the file.

```bash

chgrp hacker /flag
cat /flag
```
### topics learnt
Learned how to use chgrp to change the group associated with a file, which is another way to manage access permissions.

### reference 
NA

## challenge
fun with group names

### flag
pwn.college{k6vD7RC7lCzDfFIzSv-a1gNqKHk.dJzNyUDL5gDN1czW}

To solve this, I first ran the id command to see all the groups my user belonged to. I noticed a special group in the list. I used chgrp to assign the /flag file to that special group, which then gave me the access I needed to read it.

```bash

id
chgrp grp22724 /flag
cat /flag
```
### topics learnt
Learned that the id command is useful for checking your user's groups, which can be important for file permissions.

### reference 
NA

## challenge
changing permissions

### flag
pwn.college{A2IyqLZ0CmHO0YeZo3DqM9-0wzb.dNzNyUDL5gDN1czW}

The /flag file was not readable by anyone. I used the chmod command to add read permissions for the user, group, and others (ugo+r). After making it readable for everyone, I could simply cat the file to get the flag.

```bash

ls -l /flag
chmod ugo+r /flag
cat /flag
```
### topics learnt
Learned how to add permissions to a file using the symbolic + format in chmod.

### reference 
NA

## challenge
Executable files

### flag
pwn.college{gGuE71C95maMz2-ytL0_xhE4zVP.dJTM2QDL5gDN1czW}

The challenge program /challenge/run wasn't executable. I used ls -l to check its permissions and saw it was missing the 'x' bit. I used chmod ugo+x to add execute permission for everyone, and then I was able to run the program to get the flag.

```bash

ls -l /challenge/run
chmod ugo+x /challenge/run
/challenge/run
```
### topics learnt
Learned that files need execute permission (x) to be run as programs, and how to add it using chmod.

### reference 
NA

## challenge
Permission Tweaking practice

### flag
pwn.college{gZPpE9__r_QYBaJZ6qnBMEXGn5D.dBTM2QDL5gDN1czW}

This challenge was a series of 8 puzzles where I had to add or remove specific permissions from a file using + and -. After I successfully completed all the steps, I was given access to the /flag file, which I then made readable and used cat on.

```bash

/challenge/run
chmod go+x /challenge/pwn
chmod go-x /challenge/pwn
chmod go-r /challenge/pwn
chmod g+w /challenge/pwn
chmod go-x /challenge/pwn
chmod uo+x /challenge/pwn
chmod u-rw /challenge/pwn
chmod o+x /challenge/pwn
chmod ugo+r /flag
cat /flag
```
### topics learnt
Got a lot of practice using symbolic modes (+ and -) to fine-tune file permissions.

### reference 
NA

## challenge
Permission setting practice

### flag
pwn.college{AgEYmL_8k7qY6mFJ-vjoZGw5aAl.dNTM5QDL5gDN1czW}

This was another 8-level practice challenge. This time, I learned how to set permissions exactly using the = operator, instead of just adding or removing them. After passing the levels, I set /flag to be readable and got the flag.

```bash

/challenge/run
chmod u=r,g=rw,o=r /challenge/pwn
chmod u=-,g=-,o=rw /challenge/pwn
chmod u=wx,g=x,o=x /challenge/pwn
chmod u=rw,g=x,o=rw /challenge/pwn
chmod u=w,g=rwx,o=rwx /challenge/pwn
chmod u=r,g=rx,o=x /challenge/pwn
chmod u=rx,g=rx,o=rwx /challenge/pwn
chmod u=rx,g=rw,o=rwx /challenge/pwn
chmod u=r,g=r,o=r /flag
cat /flag
```
### topics learnt
Learned how to use the = operator with chmod to set exact permissions for user, group, and other all at once.

### reference 
NA

## challenge 
The SUID bit
### flag
pwn.college{Y1w_uktPHUVn2X6CJm4h6DWghCA.dNTM2QDL5gDN1czW}

This challenge was about the SUID bit. The /challenge/getroot program couldn't read /flag at first. I added the SUID permission using chmod u+s. This allowed the program to run with the owner's privileges (root). When I ran it again, it had the power to read the flag for me.

```bash

chmod u+s /challenge/getroot
/challenge/getroot
```
### topics learnt
Learned that setting the SUID bit (u+s) on an executable makes it run with the permissions of the file owner, not the user who runs it.

### reference
NA
