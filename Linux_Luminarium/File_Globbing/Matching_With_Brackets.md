# Matching With []
The challenge asks you to open the terminal in the pwn.college DOJO and use `[]` to glob for multiple files.

## My Solve
**Flag:** `pwn.college{kNiWzMN4lMFvmB3xdtIOgUq8n4h.QXzIDO0wCMxAzNzEzW}`

We can use `[]` to glob for multiple files all at the same time. The contents of `[]` consist of the single-character wildcards, so we could technically think of the technique as a collection of `?` characters, used to search for files and directories which have something common in their names or paths. For example, in this challenge, inside `/challenge/files`, there are files named 'file_a', 'file_b', 'file_s' and 'file_h'. After cd'ing into this directory, we can run `/challenge/run file_[absh]` to invoke all these files together in one argument. Here, `file_` is outside the square brackets as it is common to all files. Inside the square brackets, each character is considered a single-character wildcard, acting like a `?`.


```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{kNiWzMN4lMFvmB3xdtIOgUq8n4h.QXzIDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about how we can use `[]` to glob for multiple files all in one argument and without having to write filepaths multiple times. This is extremely useful when we have to execute many different programs all at once.

## References
None.