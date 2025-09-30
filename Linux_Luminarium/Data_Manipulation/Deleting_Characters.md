# Deleting Characters 
The challenge asks you to open the terminal in the pwn.college DOJO and delete decoy characters.

## My Solve
**Flag:** `pwn.college{kv0vcZpA6EhVcsPvGJp-1UW6UI8.0FNxEzNxwCMxAzNzEzW}`

We already saw how we can use `tr` to replace characters or text in general. But a variant of `tr` can also be used to entirely delete whichever characters we wish to from the stdout of a command. This is done using `tr -d`, after which we type out the characters we wish to be deleted as the argument. Here, we are still replacing characters, only with nothing. For this challenge, we must remove decoy characters from the flag given by the run command. Hence, we execute, `/challenge/run | tr -d ^%`

```
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{kv0vcZpA6EhVcsPvGJp-1UW6UI8.0FNxEzNxwCMxAzNzEzW}
```


## What I Learned
I learnt about how we can also delete text using the `tr` command, essentially replacing characters with nothing.

## References
None.