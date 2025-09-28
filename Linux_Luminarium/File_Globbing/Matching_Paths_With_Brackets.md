# Matching Paths With Brackets
The challenge asks you to open the terminal in the pwn.college DOJO and use `[]` to glob for multiple files, but this time without cd'ing into the directory.

## My Solve
**Flag:** `pwn.college{EeS537uSXKeOunOD6kow6yroh1Z.QX0IDO0wCMxAzNzEzW}`

As we learned in the previous challenge, `[]` can be used to glob for multiple files at once. However, we only tried this with just the file. We can also use this globbing technique within a path. This challenge asks you to run the `/challenge/run` command with the argument being the full path of the files (file_b,file_a,etc.) located in the `/challenge/files` directory. For this, we execute `/challenge/run /challenge/files/file_[bash]`, which gives us the flag.


```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{EeS537uSXKeOunOD6kow6yroh1Z.QX0IDO0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt how we can use the `[]` globbing technique in association with a filepath, which is how we will normally be using these globbing techniques.

## References
None.