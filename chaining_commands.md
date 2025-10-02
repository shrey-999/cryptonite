# Module Name
Chaining Commands

## challenge

chaining with semicolon

### flag

pwn.college{J9zQwE4rLpG7kF2hVbNnMcXzY1a.dVTN4QDL5gDN1czW}

For this, I had to run two programs back-to-back. Instead of typing them on separate lines and hitting enter each time, I just put a semicolon `;` between them. This runs the first command, and then the second command right after, automatically.

```bash
/challenge/pwn; /challenge/college
```

### topics learnt

Learned how to chain multiple commands together on a single line using the semicolon.

### references 

na

## challenge

Building on success

### flag

pwn.college{tG6rF9zVbN2mKlPqW4sEdRtYhUj.QXyQzM4EDL5gDN1czW}

In this challenge, the second program was only supposed to run if the first one succeeded. I used the `&&` operator to do this. The second command only executes if the first command finishes without any errors.

```bash
/challenge/first-success && /challenge/second
```

### topics learnt

Learned that `&&` links commands so that the next one only runs if the previous one was successful.

### references 

na

## challenge

handling failures

### flag

pwn.college{pL8kJuH7yGtF5rD4sW3aQ2zXcVb.QXzQzM4EDL5gDN1czW}

This was the opposite of the last one. I needed the second command to run only if the first one failed. I used the `||` operator, which acts as a fallback. If the first command produces an error, the second one will run.

```bash
/challenge/first-failure || /challenge/second
```

### topics learnt

Learned to handle command failures using `||`, which runs the second command only if the first one fails.

### references 

na

## challenge

Your first shell

### flag

pwn.college{ZxCvB5n M2lKjHgF7dSaQ1wE4rT.dFzN4QDL5gDN1czW}

This was my first time making a shell script. I used `nano` to create a file named `x.sh`. Inside the file, I just wrote the commands I needed to run. After saving the file, I ran it using `bash x.sh`.

```bash
# First, create the script file
nano x.sh

# Inside nano, I wrote this:
# /challenge/pwn && /challenge/college

# Then, run the script from the terminal
bash x.sh
```

### topics learnt

Learned how to create a simple script using `nano`, save it, and then execute it using the `bash` command.

### references 

na

## challenge

Redirecting Script Output

### flag

pwn.college{O9iU8yT6rE5wQ4aZ2sX1dC3fVbN.dhTM5QDL5gDN1czW}

Here, I needed to take the output from my script and send it directly to another program. I used the pipe `|` operator for this. I made a script `x.sh` and then ran `bash x.sh | /challenge/solve` to feed its output to the solver program.

```bash
# I created x.sh using nano and put this inside:
# echo "some_text_for_the_solver"

# Then I ran this command:
bash x.sh | /challenge/solve
```

### topics learnt

Learned how to pipe `|` the output of one script or command directly into the input of another command.

### references 

na

## challenge

Executable Shell Scripts

### flag

pwn.college{M7nB6vC5xZ4lKjHgF1dSaQ2wE3r.dRzNyUDL5gDN1czW}

I learned how to make a script runnable without typing `bash` in front of it. After creating my `x.sh` file, I used `chmod u+x x.sh` to give it execute permissions. After that, I could run it directly from my terminal using `./x.sh`.

```bash
nano x.sh
ls -l x.sh
chmod u+x x.sh
ls -l x.sh
./x.sh
```

### topics learnt

Learned how to make a script executable with `chmod +x` and run it directly with `./`.

### references 

na

## challenge

Understanding Shebangs

### flag

pwn.college{Q1wS3eD5fT7gH9jK2lZ4xV6bN8m.QX5MzM4EDL5gDN1czW}

The shebang is the first line of a script that tells the system what interpreter to use. I created a script called `solve.sh` and put `#!/bin/bash` at the very top. Then I made it executable and ran it directly.

```bash
# Create the script with nano
nano solve.sh

# This is the content of solve.sh:
# #!/bin/bash
# /challenge/run

# Make it executable and run it
chmod u+x solve.sh
./solve.sh
```

### topics learnt

Learned that adding a shebang like `#!/bin/bash` to the first line of a script defines how it should be executed.

### references 

na

## challenge

Scripting with arguments

### flag

pwn.college{P0oI9uY7tT6rE5wQ4aZ3sX2dC1f.QX1MzM4EDL5gDN1czW}

This was about using arguments with a script. I learned that `$1` represents the first argument, `$2` the second, and so on. I wrote a script that would take two arguments and print them back out in reverse order.

```bash
# Content of solve.sh:
# #!/bin/bash
# echo "$2 $1"

# The challenge ran it like: ./solve.sh arg1 arg2
/challenge/run
```

### topics learnt

Learned how to access command-line arguments inside a script using variables like `$1` and `$2`.

### references 

na

## challenge

Scripting with conditionals

### flag

pwn.college{L5k4J3hG2fD1sA8zX7cV9bN0mQ1.QX2MzM4EDL5gDN1czW}

I started using logic in my scripts with an `if` statement. I wrote a script that checked if the first argument `$1` was equal to the string "pwn". If the condition was true, it would print "college".

```bash
# Content of solve.sh:
# #!/bin/bash
# if [ "$1" == "pwn" ]
# then
#   echo "college"
# fi

/challenge/run
```

### topics learnt

Learned the basic syntax for an `if` statement in a shell script to run code based on a condition.

### references 

na

## challenge

Scripting with Default Cases

### flag

pwn.college{T4rE3wQ2aZ1sX8dC7fV6gB5hN9j.QX3MzM4EDL5gDN1czW}

I added an `else` block to my `if` statement. This allows the script to do something else if the condition is false. The script checks for "pwn", and if the input is anything else, it prints a default message.

```bash
# Content of solve.sh:
# #!/bin/bash
# if [ "$1" == "pwn" ]
# then
#   echo "college"
# else
#   echo "nope"
# fi

/challenge/run
```

### topics learnt

Learned how to use an `if/else` block to handle both the success and failure of a condition.

### references 

na

## challenge

Scripting with multiple conditions

### flag

pwn.college{U7yG6tF5rD4sW3aQ2zX1cV9bN8m.QX4MzM4EDL5gDN1czW}

To handle several different possible inputs, I used `elif` (which means "else if"). This lets you chain multiple checks together. The script checks for "hack", then "pwn", then "learn", and has a final `else` for anything that doesn't match.

```bash
# Content of solve.sh:
# #!/bin/bash
# if [ "$1" == "hack" ]
# then
#   echo "the planet"
# elif [ "$1" == "pwn" ]
# then
#   echo "college"
# else
#   echo "unknown"
# fi

/challenge/run
```

### topics learnt

Learned how to use `elif` to test for multiple different conditions in a single `if` block.

### references 

na

## challenge

Reading Shell scripts

### flag

pwn.college{J2hG4fD6sA8zX7cV5bN3mQlK1jH.QXyADO4EDL5gDN1czW}

For this one, I couldn't guess the password. So, I just used `cat` to read the script's source code. Inside the file, I saw the exact string it was checking for. I then ran the program and typed in the password to get the flag.

```bash
cat /challenge/run
/challenge/run
hack the PLANET
```

### topics learnt

Learned that sometimes the easiest way to solve a challenge is to just read the code of the script to see how it works.

### references 

na
