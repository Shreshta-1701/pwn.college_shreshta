# Translating Characters 
The challenge asks you to open the terminal in the pwn.college DOJO and toggle the case of the flag characters.

## My Solve
**Flag:** `pwn.college{oBo3MYNrQvARa2cEZM7mXr4W9Vb.01MxEzNxwCMxAzNzEzW}`

In this challenge, we are told that `/challenge/run` gives us the flag, but all it's characters have had their case switched. So all uppercase letters have been turned into lowercase letters and vice versa. We could manually switch these cases and find the flag, but that would be extremely tedious. Instead, we can use the `tr` or translate command, which allows us to essentially replace characters. For example, `echo OPWN | tr OP AB` would give us the output `ABWN`, replacing all instances of 'OP' with 'AB' in the stdout of `echo OPWN`. For this challenge, if we use `tr --help`, then we find out that `[:upper:]` and `[:lower:]` can be used instead of typing out all characters. Hence, our command to execute becomes, `/challenge/run | tr '[:upper:]''[:lower:]' '[:lower:]''[:upper:]'`.


```
hacker@data~translating-characters:~$ /challenge/run | tr '[:upper:]''[:lower:]' '[:lower:]''[:upper:]'
yOUR CASE-SWAPPED FLAG:
pwn.college{oBo3MYNrQvARa2cEZM7mXr4W9Vb.01MxEzNxwCMxAzNzEzW}
```


## What I Learned
I learnt about how we can replace text of any kind using the `tr` command, and how we can use this directly with commands by using the pipe operator.

## References
None.