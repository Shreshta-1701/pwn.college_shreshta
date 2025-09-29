# Filtering With Grep -v
The challenge asks you to open the terminal in the pwn.college DOJO and grep through command outputs while filtering out terms based on a common term.

## My Solve
**Flag:** `pwn.college{wRIpnz3hRfKK2MqUuUPWIES-92p.0FOxEzNxwCMxAzNzEzW}`

So far, we have been using the `grep` command to find the terms that are the closest matches to the search terms. But this command also has an option that is very useful to perform the opposite function. `grep -v` searches for and shows the lines that do not match the search term that is entered after the command. In this challenge, the stdout for `/challenge/run` contains many decoy flags, but all of them have the term DECOY associated with them. Hence, we can filter out the term `DECOY` using `grep -v` and get the flag. The command for this is `/challenge/run | grep -v DECOY`. This gives us the flag.


```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{wRIpnz3hRfKK2MqUuUPWIES-92p.0FOxEzNxwCMxAzNzEzW}
```


## What I Learned
I learnt about a new variant of the grep command that can be extremely useful for filtering out lines in a file or stdout in our case, and I was able to apply this knowledge to filter out decoy flags from the stdout of a command.

## References
None.