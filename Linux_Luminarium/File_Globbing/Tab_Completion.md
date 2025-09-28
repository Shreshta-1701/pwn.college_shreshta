# Tab Completion
The challenge asks you to open the terminal in the pwn.college DOJO and use the tab key to autocomplete the command/filepath that we are currently entering in the terminal.

## My Solve
**Flag:** `pwn.college{07bYB0f_RlnOtS8JnobAmVvO9mg.0FN0EzNxwCMxAzNzEzW}`

This challenge asks us to use tab completion to autocomplete a command in the terminal. Always using globbing techniques such as `*` is risky and likely won't always give us the intended results. Instead of this, whenever entering a command, or a filepath, or an argument inside a terminal, we can enter the tab key. Doing this, asks the shell to try and figure out what you're typing, and then automatically complete it. In this challenge, after entering `cat /challenge/pwn`, we can enter the tab key, to autocomplete it to `cat /challenge/pwn`, at which point, pressing enter would execute the command and give us the flag.


```
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​ 
pwn.college{07bYB0f_RlnOtS8JnobAmVvO9mg.0FN0EzNxwCMxAzNzEzW}
```


## What I Learned
I was able to learn how we can use tab completion to reduce the time wasted in typing out commands and filepaths, while not having to depend on inaccurate globbing techniques.

## References
None.