# Setting Variables
The challenge asks you to open the terminal in the pwn.college DOJO and then set a variable to a specific value.

## My Solve
**Flag:** `pwn.college{0k_XsG6X9M7fAm-B2R0Piff0woG.QX5UTN0wCMxAzNzEzW}`

In this challenge, we are tasked with having to set a value to a variable. To do this, we use `=`. For example, in this challenge, `PWN=COLLEGE` sets the value `COLLEGE` to the `PWN` variable. We do not use `$` here, as that is used only to access the variable. There are two other things which we also must remember. There should be no space around the `=` character, as that would lead to the shell thinking of `PWN` as a command. Also, these variables are case-specific. 


```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{0k_XsG6X9M7fAm-B2R0Piff0woG.QX5UTN0wCMxAzNzEzW}
```


## What I Learned
I learnt how to set variables to a specific value and also about all the different guidelines related to using the `=` character to assign values to a variable.`

## References
None.