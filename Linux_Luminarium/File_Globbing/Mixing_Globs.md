# Mixing Globs
The challenge asks you to open the terminal in the pwn.college DOJO and use mix different globbing techniques all at once to execute the run command with the correct argument and get the flag.

## My Solve
**Flag:** `pwn.college{w5C5qOgV-RyEiZFuhdGMtfmrYi6.QX1IDO0wCMxAzNzEzW}`

In this challenge, we learn how to mix together different globbing techniques. This allows us to further shorten our filepaths and expand our searching criteria, as different globs can allow us to search for different files easily. Let's take this challenge as an example. We first cd into the `/challenge/files`. Then, we have been asked to invoke the `/challenge/run` with the arguments that match the three files named `challenging, educational and pwning`, while keeping the argument six characters or lesser in size. Hence, we run `/challenge/run [cep]*`, where `[cep]` uses the brackets globbing technique to glob for files starting with c, e or p. Then the `*` character globs for files that have anything after the beginning characters. Executing this command gives us the flag.


```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{w5C5qOgV-RyEiZFuhdGMtfmrYi6.QX1IDO0wCMxAzNzEzW}
```


## What I Learned
In this challenge, I learnt how we can mix multiple globbing techniques together to glob for different files with different search criterias all at once.

## References
None.