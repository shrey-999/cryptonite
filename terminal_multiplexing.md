# Module Name

Terminal Multiplexing

## challenge

Launching screen

### flag

pwn.college{W3rT5yU7iO9pA1sD2fG4hJ6kL8z.QX1gjM4EDL5gDN1czW}

To solve this, I just had to type `screen` in the terminal. This launched a new virtual terminal session right inside my current one, and the flag was waiting there.

```bash
screen
```

### topics learnt

Learned how to launch a new virtual terminal session using the `screen` command, which is like opening a new tab.

### references

na

## challenge

Detaching and Attaching

### flag

pwn.college{M1nB2vC3xZ4lKjHgF7dSaQ5wE6r.QX2gjM4EDL5gDN1czW}

I started a `screen` session, then detached from it by pressing the key combination `Ctrl+a` then `d`. This let the session run in the background. After running the challenge program, I reattached to the session using `screen -r` to see the result.

```bash
screen
# Press Ctrl+a, then d to detach
/challenge/run
screen -r
```

### topics learnt

Learned how to detach from a screen session to let it run in the background and reattach to it later.

### references

na

## challenge

finding sessions

### flag

pwn.college{P0oI9uY8tT7rE6wQ5aZ4sX3dC2f.QX3gjM4EDL5gDN1czW}

This challenge had multiple screen sessions running. I used `screen -ls` to list all of them and see their names. Then I had to attach to each one using `screen -r <session_name>` until I found the one that had the flag.

```bash
screen -ls
screen -r session_fe99b74255972c82
```

### topics learnt

Learned how to list all active screen sessions and attach to a specific one by its name or PID.

### references

na

## challenge

switching windows

### flag

pwn.college{G4hJ6kL8zX7cV5bN3mQlKwE2rT9.QX4gjM4EDL5gDN1czW}

Inside a `screen` session, you can have multiple windows. I reattached to the running session, and the flag was in a different window. I switched to window 0 by pressing `Ctrl+a` then `0` to get the flag.

```bash
screen -r
# Press Ctrl+a, then 0
```

### topics learnt

Learned how to switch between different windows inside a single screen session using `Ctrl+a` followed by the window number.

### references

na

## challenge

Detaching and Attaching(tmux)

### flag

pwn.college{A1sD2fG4hJ6kL8zX7cV5bN3mQlK.QX5gjM4EDL5gDN1czW}

This was similar to screen, but with `tmux`. I started a session with `tmux`. The key combination to detach is `Ctrl+b` then `d`. After detaching, I ran the program and reattached using `tmux a`.

```bash
tmux
# Press Ctrl+b, then d
/challenge/run
tmux a
```

### topics learnt

Learned the basics of `tmux`, including its default prefix `Ctrl+b` for commands like detaching.

### references

na

## challenge

switching windows (tmux)

### flag

pwn.college{L8kJuH7yGtF6rD5sW4aQ3zX2cV1.QXwkjM4EDL5gDN1czW}

Just like with screen, `tmux` can have multiple windows. After attaching to the session with `tmux a`, I needed to switch to window 0. The command for this in tmux is `Ctrl+b` then `0`, which brought me to the flag.

```bash
tmux a
# Press Ctrl+b, then 0
```

### topics learnt

Learned how to switch between windows in a `tmux` session, using the `Ctrl+b` prefix followed by the window number.

### references

na
