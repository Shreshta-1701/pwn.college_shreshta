# Touching Files
The challenge asks you to open the terminal in the pwn.college DOJO and create some files in the `/tmp` directory and then invoke the run program to find the flag.

## My Solve
**Flag:** `pwn.college{UqKqjnqu1ZxxSQZo15oW6Ng0jA3.QXwMDO0wCMxAzNzEzW}`

In this challenge, we use the `touch` command, which allows us to create new files just by naming them as a part of the path we want them to be located. For example, if we want to create a file called 'pwn' inside the '/tmp' directory, we simply need to execute the command `touch /tmp/pwn`. This will create the 'pwn' file inside the 'tmp' directory. Similary we can create a `college` file within the same directory. Then, we can invoke `/challenge/run` to get the flag. If instead of specifying a path in the argument for the `touch` command, we simply write the name of the file to be created and it's type, then the file would be created in the `cwd`.

```
hacker@commands~touching-files:~$ touch /tmp/pwn /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{UqKqjnqu1ZxxSQZo15oW6Ng0jA3.QXwMDO0wCMxAzNzEzW}
```

## What I Learned
I learnt the use of the `touch` command which can be used to create files with ease without having to leave the terminal or use a file explorer. This command comes in handy esspecially when working with projects on Github, like for these writeups, where we can simply use the touch command once to create empty markdown files for all writeups at once, without having to navigate to the repository in our file explorer and then creating the files one by one.

## References
None.