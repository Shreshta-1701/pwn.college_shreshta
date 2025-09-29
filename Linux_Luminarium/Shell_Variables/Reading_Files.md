# Reading Files 
The challenge asks you to open the terminal in the pwn.college DOJO and read a file into a variable.

## My Solve
**Flag:** `pwn.college{QWq8o8J7NIHfwMx63-F5dF-mz3u.QXwIDO0wCMxAzNzEzW}`

While you can use `cat` to read a file and then store the output of the cat command in a variable, doing so is not the most convenient way or reading files in a shell and storing them in variables. Instead, we can use the `read` command that we learned recently. In this challenge, entering `read PWN < /challenge/read_me` automatically reads the read_me file into the PWN variable all in one line. This gives us the flag.

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{QWq8o8J7NIHfwMx63-F5dF-mz3u.QXwIDO0wCMxAzNzEzW}
```

## What I Learned
I learnt how we can read entire files into variables without using the `cat` command.

## References
None.