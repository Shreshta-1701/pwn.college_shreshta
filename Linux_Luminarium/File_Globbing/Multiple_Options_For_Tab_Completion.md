# Multiple Options For Tab Completion
The challenge asks you to open the terminal in the pwn.college DOJO and use the tab key to autocomplete the command/filepath that we are currently entering in the terminal, but this time, amongst multiple matching files.

## My Solve
**Flag:** `pwn.college{oTL2zBT-96wByT_UaY157oWiN0C.0lN0EzNxwCMxAzNzEzW}`

In this challenge, we use tab completion to read the flag file. But, there are multiple files with similar names, and hence tab completion won't give us the answer straight away. Instead, we will have to keep trying multiple times if we want to invoke the intended file. For example, when entering `cat /challenge/files/p` and then tab, it autocompletes to `cat /challenge/files/pwn`. Now, in bash, when you hit tab again after it has already matched with the first result, then it prints out all the other possible results. Then, we can see the `pwncollege-flag` file, which is most likely to hold the flag. Then, we use tab completion to move to that file, and read it using `cat` to get the flag.


```
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-college            pwn-the-planet         pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{oTL2zBT-96wByT_UaY157oWiN0C.0lN0EzNxwCMxAzNzEzW}
```


## What I Learned
I was able to learn how we can use tab completion even when there are multiple files matching the same criteria, and how we can print them all out and further press tab to move to the correct one. In other shells, we don't even need to print the matches out, as pressing tab would keep cycling through the different possible matches, making the entire process much easier.

## References
None.