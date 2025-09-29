# Grepping Stored Results
The challenge asks you to open the terminal in the pwn.college DOJO and redirect output to another file, and then grep that file to get the flag.

## My Solve
**Flag:** `pwn.college{wzpfXmZhr8EyBAeaZbwOJnrMuxU.QX4EDO0wCMxAzNzEzW}`

We have learned how to redirect command outputs to files, and we can now combine this with our previous knowledge of the `grep` command. First, we redirect the output of `/challenge/run` to `/tmp/data.txt` by executing the command `/challenge/run > /tmp/data.txt`. After doing this, we can grep the `/tmp/data.txt` file for the flag. We already know that the flag always contains the text 'pwn.college', so we can use that as our search term. Hence, we execute `grep pwn.college /tmp/data.txt` which gives us the flag.


```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{wzpfXmZhr8EyBAeaZbwOJnrMuxU.QX4EDO0wCMxAzNzEzW}
```


## What I Learned
I put into practice my previous knowledge of the `grep` command and my newly learned knowledge about redirecting outputs to redirect the output of a command to a file, and then grep that file for a certain flag.

## References
None.