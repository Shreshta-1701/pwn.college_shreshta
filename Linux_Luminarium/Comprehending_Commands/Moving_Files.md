# Moving Files
The challenge asks you to open the terminal in the pwn.college DOJO and move a flag file from one directory to another, and then invoke the check program to find the flag.

## My Solve
**Flag:** `pwn.college{ICNXIUmXU4C8z8yNKGMBJVwj8va.0VOxEzNxwCMxAzNzEzW}`

In this challenge, we use the `mv` (move) command, which is used to move files from place to another. Essentially like cutting and pasting something. The command takes 2 arguments. The first being the path of the file we want to move, and the second argument is the path where we want the file to be moved to. For this challenge, the command to move `/flag` to `/tmp/hack-the-planet` is `mv /flag /tmp/hack-the-planet`. After this, we can invoke `challenge/check` and get the flag.

```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{ICNXIUmXU4C8z8yNKGMBJVwj8va.0VOxEzNxwCMxAzNzEzW}
```

## What I Learned
I learnt how we can use the `mv` command to move files from directory to another through the terminal itself, adding to our collection another terminal command that can be used to operate on files directly.

## References
None.
