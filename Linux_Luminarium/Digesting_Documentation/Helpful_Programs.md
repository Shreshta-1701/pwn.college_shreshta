# Helpful Programs
The challenge asks you to open the terminal in the pwn.college DOJO and use a command to get information on how to access the flag using the correct arguments.

## My Solve
**Flag:** `pwn.college{4fs85eHjKzXvKuBIqGPBlwyhZJE.QX3IDO0wCMxAzNzEzW}`

All commands don't have a manpage, but information about their functions and arguments can still be accessed using the `--help` or `-h` argument after the command. Over here, we execute `/challenge/challenge --help` to open the help documentation for the `/challenge/challenge` command. Then, we can see that the argument `-g` gives us the flag if executed with a certain value. We can also see that this value can be printed onto the terminal by using the argument `-p`. Hence, executing `/challenge/challenge -p`, we get the secret value, that is '485'. Using this, we exectute `/challenge/challenge -g 485`, which gives us the flag.


```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 485
hacker@man~helpful-programs:~$ /challenge/challenge -g 485
Correct usage! Your flag: pwn.college{4fs85eHjKzXvKuBIqGPBlwyhZJE.QX3IDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about the fact that even though not all commands have manpages, we can still learn about them using the `-h` command. I also learnt about the different variations of the `-h` command, which are `--help`, `-?`, `help`, and sometimes even `/?`.

## References
None.