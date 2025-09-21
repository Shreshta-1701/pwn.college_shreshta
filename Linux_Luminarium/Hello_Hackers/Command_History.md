# Command History
The challenge asks you to open the terminal in the pwn.college DOJO and use the arrow keys to scroll through the command history in the terminal and find the flag.

## My Solve
**Flag:** 'pwn.college{kDEScc1SxmrA8JpTi-lmLGtgjNz.0lNzEzNxwCMxAzNzEzW}'

Linux commands are stored in the memory during each terminal session, and hence we can use the arrow keys to navigate the history of commands that we entered during that specific session.

Using this knowledge, we can press the up arrow key to go back and get the flag from the terminal's history.

```
hacker@hello~command-history:~$ <UP ARROW PRESSED>
hacker@hello~command-history:~$ the flag is pwn.college{kDEScc1SxmrA8JpTi-lmLGtgjNz.0lNzEzNxwCMxAzNzEzW}```

## What I Learned
I was able to learn that the Linux Terminal stores the command history of a session, and we can use previous commands by navigating through the history using the up and down arrow keys.

## References
None.