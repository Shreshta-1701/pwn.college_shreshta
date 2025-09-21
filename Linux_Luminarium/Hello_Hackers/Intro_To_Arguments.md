# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'echo' and 'hello' commands with multiple arguments to obtain different results.

## My Solve
**Flag:** 'pwn.college{8yVf40kJCDaZBu31EvwbUtRcKrK.QX4YjM1wCMxAzNzEzW}'

First we execute the 'echo' command in the terminal. This command can take any amount of arguments. If we type 'echo Hello', then the command has only one argument, and it displays 'Hello' in the terminal. If we pass 2 arguments to the command, like in 'echo Hello Hackers!', (The 2 arguments being Hello and Hackers!) then the output changes to 'Hello Hackers!'. 
In a similar way, we can use the 'hello' command with the 'hackers' argument, to obtain the flag.

```
hacker@hello~intro-to-arguments:~$ echo Hello
Hello
hacker@hello~intro-to-arguments:~$ echo Hello Hackers!
Hello Hackers!
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{8yVf40kJCDaZBu31EvwbUtRcKrK.QX4YjM1wCMxAzNzEzW}
```

## What I Learned
I learnt how Linux commands can take up multiple arguments and how these arguments can be altered to obtain different outputs in the terminal. I also learned the function of the 'echo' command, which essentially echoes the arguments we enter, back as output in the terminal. Pretty much like a print statement in programming languages.

## References
None.