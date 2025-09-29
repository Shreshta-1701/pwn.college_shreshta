# Grepping Live Output
The challenge asks you to open the terminal in the pwn.college DOJO and grep a command's output for the flag without using an output file.

## My Solve
**Flag:** `pwn.college{YdtE676Ud2lw3Wc0uV8v_WNpiOQ.QX5EDO0wCMxAzNzEzW}`

We already learnt how to grep through output files to find certain text in a command output. But we can actually cut out this middleman that is the output file, by using something known as the **pipe operator** or `|`. To the left of this pipe, is the command that we need to redirect the output of, while to its right is the grep command, which directly greps through the output of the command, without ever having to access or even create an output file. For example, in this challenge, we execute `/challenge/run | grep pwn.college` to grep for the term **pwn.college** throughout the output of the `/challenge/run` command. This gives us the flag.


```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{YdtE676Ud2lw3Wc0uV8v_WNpiOQ.QX5EDO0wCMxAzNzEzW}
```


## What I Learned
I learnt how we can get rid of the need of output files when grepping for terms in command outputs, and use the `|` operator to combine the command and the grep statement together in one line.

## References
None.