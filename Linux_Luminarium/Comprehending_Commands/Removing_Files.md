# Removing Files
The challenge asks you to open the terminal in the pwn.college DOJO and delete a file in the home directory and then invoke the run program to find the check.

## My Solve
**Flag:** `pwn.college{EWjq2tHtN4eoXZ-McfbEZfjt6Ap.QX2kDM1wCMxAzNzEzW}`

In the previous challenge, we created files using the `touch` command. In this challenge, we will use the `rm` (remove) command to delete any file. The command can be executed in a similar way as the `touch` command, even taking the same type of arguments as it. For this challenge, we need to delete a file already present in the home directory, which as we already know, is always our `cwd` when we first open the pwn.college DOJO Terminal. Hence, we can run the command `rm delete_me` to delete the specified file. Then, we can invoke `/challenge/check` to get the flag.

```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{EWjq2tHtN4eoXZ-McfbEZfjt6Ap.QX2kDM1wCMxAzNzEzW}
```

## What I Learned
I learnt how we can use the `rm` command to remove any files we wish to get rid of. This prevents unnecessary bloating of the computer and allows us to make our workflow more organised, as being able to remove unnecessary files is a basic operation that any system should be capable of.

## References
None.
