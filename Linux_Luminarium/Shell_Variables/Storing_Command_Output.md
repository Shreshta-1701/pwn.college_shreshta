# Storing Command Output
The challenge asks you to open the terminal in the pwn.college DOJO and store the value of a command in a variable and then print that variable.

## My Solve
**Flag:** `pwn.college{YGIQ8dKPyPifVwKvMhiK6EBHnGt.QX1cDN1wCMxAzNzEzW}`

In this challenge, we have been tasked with storing command outputs in variables. We can do so with the syntax `VAR=$(command)`. Over here, the output of the command would be stored in the VAR variable. Similarly, for this challenge, we execute `PWN=$(/challenge/run)`, which stores the output of the `/challenge/run` command in the PWN variable. After this, we can print out the variable by executing `echo $PWN`, which gives us the flag.

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{YGIQ8dKPyPifVwKvMhiK6EBHnGt.QX1cDN1wCMxAzNzEzW}
```

## What I Learned
I learnt how we can store command outputs in variables, allowing us to reuse commands that might come in handy multiple times.

## References
None.