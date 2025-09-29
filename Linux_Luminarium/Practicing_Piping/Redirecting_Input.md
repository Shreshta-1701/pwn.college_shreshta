# Redirecting Input
The challenge asks you to open the terminal in the pwn.college DOJO and redirect input to another file.

## My Solve
**Flag:** `pwn.college{Q738g_Z0v8_zOgwjmYbmGapOS8p.QXwcTN0wCMxAzNzEzW}`

In this challenge, we are first asked to redirect the output of `echo COLLEGE` to the `PWN` file. For this, we execute `echo COLLEGE > PWN`. After this, we have been asked to redirect this value from the PWN file to `/challenge/run`. For this, we must redirect the input to the `/challenge/run` program. This can be done by using the `<` character. This allows us to redirect inputs to programs. Hence, we execute `/challenge/run < PWN` to redirect the input from PWN to the `/challenge/run` program, which gives us the flag.


```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{Q738g_Z0v8_zOgwjmYbmGapOS8p.QXwcTN0wCMxAzNzEzW}
```


## What I Learned
I learnt how we can redirect input from files to programs, which can be used to send inputs to programs. This helps us create a workflow where we redirect outputs from certain commands to files and store them there, and then redirect the inputs from these files to other commands to get desired results.

## References
None.