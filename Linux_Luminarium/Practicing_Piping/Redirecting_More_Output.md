# Redirecting More Output
The challenge asks you to open the terminal in the pwn.college DOJO and redirect the output of a command to a file and then read that file to get the flag.

## My Solve
**Flag:** `pwn.college{MNNmdpSHUzy2RO1ubVClkgrsDLg.QX1YTN0wCMxAzNzEzW}`

This challenge allows us to further practice what we learned about redirecting outputs in the previous challenge. It asks us to redirect the output of `/challenge/run` (which gives us the flag) to the file `myflag`. Without doing so, we cannot get the flag. Hence, we execute the command `/challenge/run > myflag`. Now, since the flag from `/challenge/run` has been redirected to the file `myflag`, we can enter `cat myflag` and read the flag.


```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{MNNmdpSHUzy2RO1ubVClkgrsDLg.QX1YTN0wCMxAzNzEzW}
```


## What I Learned
I was able to further apply my knowledge of redirecting outputs and redirect the output of a command other than just `echo` to a file, and then read the file using `cat` to get the flag.

## References
None.