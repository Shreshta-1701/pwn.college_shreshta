# Extracting The First Lines With Head
The challenge asks you to open the terminal in the pwn.college DOJO and extract the first 7 lines from an stdout.

## My Solve
**Flag:** `pwn.college{M1n-nb5HmHigukmXVG-DpnMa9PU.0lNxEzNxwCMxAzNzEzW}`

We can also use the `head` command to extract the beginning portion of the standard output of a command. This is done by piping the command with `head`, just like we did for the `tr` command. By default, it displays the first 10 lines, however, this can be controlled using the `-n` option. For example, `head -n 2` prints out the first 2 lines. For this challenge, we are to execute the `/challenge/pwn` command, extract the first 7 lines from it, and pipe them to `/challenge/college`. The command for this is, `/challenge/pwn | head -n 7 | /challenge/college`

```
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{M1n-nb5HmHigukmXVG-DpnMa9PU.0lNxEzNxwCMxAzNzEzW}
```

## What I Learned
I learnt about how we can use the `head` command to extract the first few lines of the output that a command produces. I also learned how I can specify how many lines from the beginning need to be printed out, using the `-n` option.

## References
None.