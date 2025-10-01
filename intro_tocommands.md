In this challenge we will invoke our first command! When you type a command and hit enter, the command will be invoked, as so:

```bash
hacker@dojo:~$ whoami
hacker
hacker@dojo:~$ 
```

Here, the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command

In this level, invoke the hello command to get the flag! Keep in mind: commands in Linux are case sensitive: hello is different from HELLO.

by executing the prompt in the same terminal where we pass "hello" as an argument instead of whoami , we get:
```bash
ls-l flag:pwn.college{YebiQv-K30TElAQQ8siI0QJ19ep.QX3YjM1wCN5UzNzEzW}
```

