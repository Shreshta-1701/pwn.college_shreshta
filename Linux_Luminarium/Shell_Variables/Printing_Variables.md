# Printing Variables
The challenge asks you to open the terminal in the pwn.college DOJO and then print the flag variable.

## My Solve
**Flag:** `pwn.college{Q2xr3cYFUvd_M1A28fY9aYz466U.QX3UTN0wCMxAzNzEzW}`

In this challenge, we get to know about variables. We already know that the `echo` command can be used to print out statements that we enter as arguments to it. But, we can also print out variables, if we prepend them with a `$` character. For example, `echo $PWD` prints out the PWD variable, which stores the `cwd` of the terminal process. Similary, the flag has been stored in the FLAG variable, which we can print out using `echo $FLAG`.


```
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{Q2xr3cYFUvd_M1A28fY9aYz466U.QX3UTN0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt about how we can print variables onto the terminal using the `echo` command and how we can access them in the first place, which is by prepending variable names with the `$` character.

## References
None.