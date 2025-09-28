# Matching With ?
The challenge asks you to open the terminal in the pwn.college DOJO and use `?` to replace certain letters in the argument to cd and invoke the flag program.

## My Solve
**Flag:** `pwn.college{83cw2qzsKpbMdM3k-yxVm_rw5lH.QXyIDO0wCMxAzNzEzW}`

While `*` allows us to shorten filepaths by globbing entire strings, the `?` character can also be used to glob singular characters. Whenever a command sees `?` in association with what seems to be a path, it treats `?` like a single-character wildcard, meaning it replaces the character in the '?' position with the closest matching character according to the rest of the path. Similary, for this challenge, we are meant to cd into the `/challenge` directory to invoke the `/challenge/run` program to get the flag, but we must not use `c` or `l` in the argument to cd. Hence, we execute `cd /?ha??enge`, which changes the `cwd` to `/challenge`, and from here, we can execute the correct command to get the flag, which is `/challenge/run`.


```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{83cw2qzsKpbMdM3k-yxVm_rw5lH.QXyIDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about how we can use `?` to glob singular characters when working with filepaths. We can also repeat the character so that it works in a way similar to the `*` globbing technique.

## References
None.