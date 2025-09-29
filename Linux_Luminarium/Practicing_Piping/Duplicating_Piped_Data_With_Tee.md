# Duplicating Piped Data With Tee
The challenge asks you to open the terminal in the pwn.college DOJO and duplicate output to find out a secret argument.

## My Solve
**Flag:** `pwn.college{IDlFcvq0Kj14WWSNK6qDjOWsy3C.QXxITO0wCMxAzNzEzW}`

When piping data from one command to another, it can often become difficult to debug anything when something goes haywire, as yuo have nothing on the screen to go off of. To counteract this issue, we can use the `tee` command, which essentialy acts as a splitter, duplicating the command's output into multiple files. Where we can read the output file to find the problem. Let's say, for this question, we first had to execute `/challenge/pwn | /challenge/college`, but this gives us an error, telling us that the pwn command has a secret code that we do not currently know of. What we can do now is use `tee` like in `/challenge/pwn | tee cmd1_output | /challenge/college`, and then execute `cat cmd1_output` to read the output file, and this tells us the secret argument that must be used with the pwn command. Then, we execute `/challenge/pwn --secret IDlFcvq0 | /challenge/college`, which gives us the flag.


```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee cmd1_output | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat cmd1_output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "IDlFcvq0"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IDlFcvq0 | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{IDlFcvq0Kj14WWSNK6qDjOWsy3C.QXxITO0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt about the T Splitter or `tee`, which can be used to duplicate outputs which can be extremely useful when performing debugging.

## References
None.