# Reading Manuals
The challenge asks you to open the terminal in the pwn.college DOJO and pass the correct argument to the challenge program to find the flag.

## My Solve
**Flag:** `pwn.college{0kDUE74xI5eIu_L7SQLefoHlC3d.QX0EDO0wCMxAzNzEzW}`

In this challenge, we make use of the `man` (manual) command. It displays the manual or documentation of the command entered alongside it. This allows us to read through the documentation of any command that we wish to know more about, and use its different arguments for different functions. For example, in this challenge, we are meant to find out the argument to the challenge command which will give us the flag. So we enter `man challenge` to open the documentation of this command. Over there, we find an argument `--kxeuef` which states that it will give us the flag when the argument to that argument is `074`. So, we enter `/challenge/challenge --kxeuef 074`, which gives us the flag.


```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --kxeuef 074
Correct usage! Your flag: pwn.college{0kDUE74xI5eIu_L7SQLefoHlC3d.QX0EDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about how the `man` command can be used to read the Documentation of any command in Linux. I also learned that to open the documentation for any command, `man` doesn't actually interact with the file directly, which is why we don't need to enter the path of the command that we wish to read the documentation for. We can simply enter the name of the command, and this will open up a documentation page for us, which we can navigate through with the help of the arrow keys, and quit, by pressing `q`.

## References
None.