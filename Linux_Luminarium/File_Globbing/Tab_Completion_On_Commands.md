# Tab Completion On Commands
The challenge asks you to open the terminal in the pwn.college DOJO and use the tab key to autocomplete a command and execute it to get the flag.

## My Solve
**Flag:** `pwn.college{QkiVbrwnlesrxoQG6mj6mxzlivM.0VN0EzNxwCMxAzNzEzW}`

In this challenge, we make use of tab completion, but this time, with commands. Tab completion can be used to autocomplete any commands. However, one should not be reckless with it, and always make sure to double check the result of the autocompletion, before executing any commands. In this program, we are told that the command to invoke the flag starts with `pwncollege`. Hence, after entering this term in the terminal, we press tab, which autocompletes the command to `pwncollege-12278`. Executing this command gives us the flag.


```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-12278 
Correct! Here is your flag:
pwn.college{QkiVbrwnlesrxoQG6mj6mxzlivM.0VN0EzNxwCMxAzNzEzW}
```


## What I Learned
I was able to learn how we can use tab completion to autocomplete not just filepaths but also commands. I also learnt about why we should still be wary when using tab completion, as while being more accurate and safer than globbing techniques as you can double check the result, it is still not always correct.

## References
None.