# Help For Builtins
The challenge asks you to open the terminal in the pwn.college DOJO and find the argument for a builtin command that will give us the flag when executed.

## My Solve
**Flag:** `pwn.college{49lF6FPhclUR5MrBHYz_yRvJUrp.QX0ETO0wCMxAzNzEzW}`

SOme commands don't have both, manpages and help options, because they are built into the terminal shell itself. These commands are called `builtins`. An example of a builtin command is `cd`. Builtins are invoked like other commands, but the shell handles them internally instead of launching other programs from other locations. To get help with builtin commands, we can use `help` with the command for this scenario being, `help challenge`, as challenge is stated to be a builtin command. This tells us about the `--secret` argument, which when passed with the secret value (Also mentioned in the help page), gives us the flag. Hence, we run `challenge --secret 49lF6FPh` which displays the flag in return.


```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "49lF6FPh".
hacker@man~help-for-builtins:~$ challenge --secret 49lF6FPh
Correct! Here is your flag!
pwn.college{49lF6FPhclUR5MrBHYz_yRvJUrp.QX0ETO0wCMxAzNzEzW}
```


## What I Learned
I learnt about `builtin` commands and how they work differently from other commands stored on the computer. I also learnt how we can use the `help` command to learn more about builtin commands which don't have separate manpages or help options.

## References
None.