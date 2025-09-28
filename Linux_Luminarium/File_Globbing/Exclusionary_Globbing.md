# Exclusionary Globbing
The challenge asks you to open the terminal in the pwn.college DOJO and exclude certain matches from a glob argument and get the flag by invoking the run program with the right argument.

## My Solve
**Flag:** `pwn.college{A4bNMRf6TVdqaGgqfshINfg4Mq-.QX2IDO0wCMxAzNzEzW}`

In this challenge, we learn how we can exclude matches from a glob. Let's say we wish to filter out files starting with p, w and n when globbing, then we can exclude them by using the exclusionary globbing technique, `[^pwn]`, which filters out these files and globs for all files other than them. Hence, after cd'ing into `/challenge/files`, we can execute `/challenge/run [^pwn]*` to get the flag.


```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{A4bNMRf6TVdqaGgqfshINfg4Mq-.QX2IDO0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt how we can exclude/filter files from our globbing arguments, by making the first character in the square brackets `^` or `!`.

## References
None.