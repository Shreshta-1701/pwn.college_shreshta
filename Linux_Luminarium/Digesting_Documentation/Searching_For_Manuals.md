# Searching For Manuals
The challenge asks you to open the terminal in the pwn.college DOJO and find the hidden manual for the command to find the argument that will return the flag.

## My Solve
**Flag:** `pwn.college{wij2wRiaaI_O3GlVUUNj7VSN1Ot.QX2EDO0wCMxAzNzEzW}`

This challenge tells us how all `manpages` or manuals are a part of a searchable database, that can be accessed in order to find the right one. To search through this database, we must read the `manpage` of the `man` command. Hence, we execute the `man man` command. This shows us the manual page for the man command, where we can find the `-K` argument, which allows us to search for text across all manual pages, essentially a brute force search. We need to run this command and argument with `/challenge/challenge`, as the question tells us that we still must use `/challenge/challenge` to get the flag. After running this command, we find the documentation for challenge, which tells us that to get the flag, we need to enter `--wijwia 237`. So, we enter `/challenge/challenge --wijwia 237` and get the flag.


```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -K '/challenge/challenge'
^C
hacker@man~searching-for-manuals:~$ /challenge/challenge --wijwia 237
Correct usage! Your flag: pwn.college{wij2wRiaaI_O3GlVUUNj7VSN1Ot.QX2EDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about how we can search for manuals to find the right one for our command if in case it is a hidden `manpage` or is difficult to access normally. This can help us speed up our workflow as we simply need to run searches for the manual of that command and the most accurate search result will simply show up on the terminal, giving us all the information that we need.

## References
None.