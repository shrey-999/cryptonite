# Module Name

Pondering PATH

## challenge

the path variable

### flag

pwn.college{X1cV2bN3mJ4kL5pQ6wE7rT8yU9i.dZzNwUDL5gDN1czW}

In this challenge, a program was trying to delete the flag using the `rm` command. By changing the `PATH` variable to a directory that doesn't contain `rm` (like my home directory), the program couldn't find the `rm` command and failed to delete the flag, allowing me to read it.

```bash
echo $PATH
PATH="/home/hacker"
/challenge/run
```

### topics learnt

Learned that the `PATH` variable tells the shell where to look for commands. By changing it, you can effectively "disable" commands by making them impossible to find.

### references

na

## challenge

Setting Path

### flag

pwn.college{A1sD2fG4hJ6kL8zX7cV5bN3mQlK.dVzNyUDL5gDN1czW}

The challenge program needed to run another command, but it couldn't find it in the default `PATH`. I had to set the `PATH` to point to `/challenge/more_commands`. This allowed the main program to find and execute the helper command it needed to solve the challenge.

```bash
PATH="/challenge/more_commands"
/challenge/run
```

### topics learnt

Learned that you can set the `PATH` to a specific directory to allow programs to find other executables they depend on.

### references

na

## challenge

Finding Command

### flag

pwn.college{T9zX8cV7bN6mJ5kL4pQ1wE2rT3y.QX3MTM3EDL5gDN1czW}

I had to find where a command named `win` was located. I used `which win` to get the full path to its directory. Since the flag was in the same directory, I could then `cd` to that location and `cat` the flag.

```bash
which win
cd /challenge/paths/12287
ls
cat flag
```

### topics learnt

Learned how to use the `which` command to find the exact location of an executable by searching the directories listed in the `PATH` variable.

### references

na

## challenge

Adding Commands

### flag

pwn.college{YhU7jI6kL4pQwE2rT9zXvB5nM1k.dZzNyUDL5gDN1czW}

The challenge required a `win` command that didn't exist. I created my own `win` shell script that would print the flag. I made it executable with `chmod +x`. Then, I added my home directory (where I created the script) to the `PATH` variable. When the challenge ran, it found and executed my script.

```bash
# Create the 'win' script
nano win

# Inside nano, I wrote:
# #!/bin/bash
# cat /flag

# Make the script executable
chmod +x win

# Add the script's location to the PATH and run
PATH="$PATH:/home/hacker"
/challenge/run
```

### topics learnt

Learned how to add a new directory containing custom scripts to the `PATH` variable, allowing the shell to find and run them like standard commands.

### references

na

## challenge

hijacking Commands

### flag

pwn.college{G4hJ6kL8zX7cV5bN3mQlKwE2rT9.ddzNyUDL5gDN1czW}

This challenge was about PATH hijacking. A program was going to use `rm`. I created my own fake `rm` script in my home directory that just printed the flag. Then, I changed the `PATH` to put my home directory *before* the real directory that contains `rm`. When the challenge ran, the shell found my fake `rm` first and ran it, giving me the flag instead of deleting anything.

```bash
# Create a fake 'rm' script
nano rm

# Inside nano, I wrote:
# #!/bin/bash
# cat /flag

# Make the script executable
chmod +x rm

# Prepend my directory to the PATH and run
PATH="/home/hacker:$PATH"
/challenge/run
```

### topics learnt

Learned that the order of directories in the `PATH` variable matters. The shell uses the first command it finds, so you can "hijack" a command by placing a fake version in a directory that comes earlier in the `PATH`.

### references

na
