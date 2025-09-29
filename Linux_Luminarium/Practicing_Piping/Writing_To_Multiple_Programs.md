# Writing To Multiple Programs
The challenge asks you to open the terminal in the pwn.college DOJO and write a command's output to two different commands.

## My Solve
**Flag:** `pwn.college{4ah4SmrUk_dCCRFhqQkincMjd_k.QXwgDN1wCMxAzNzEzW}`

We already learnt how to use `tee` to duplicate data to two files, or to a file and a command. But, tee normally doesn't allow you to duplicate data to two commands. However, as we learned in the previous challenge, in Linux, we can turn any command into a temporary file or a `named pipe` with the following syntax - `<(command)`. We used `<` in the previous example, but over here, we use `>(command)` as we need to duplicate the data to the command, and not take data from it. This makes our final statement to be executed, according to the conditions, `/challenge/hack | tee >(/challenge/the) | /challenge/planet`, which gives us the flag.


```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{4ah4SmrUk_dCCRFhqQkincMjd_k.QXwgDN1wCMxAzNzEzW}
```


## What I Learned
In this challenge I was able to learn how we can use Process Substitution and `tee` together to write a command's output to multiple commands. I also learnt how we can duplicate data to a command in Linux, using the syntax `>(command)`.

## References
None.