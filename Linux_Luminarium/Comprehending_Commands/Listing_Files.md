# Listing Files
The challenge asks you to open the terminal in the pwn.college DOJO and list the files in a directory to find the flag file.

## My Solve
**Flag:** `pwn.college{EWwIJp2Wj1aZOABiaElNB9V-n1A.QX4IDO0wCMxAzNzEzW}`

In this challenge, we use the `ls` command. This command can be used to list all sub-directories and files located within a specific directory. It takes one or zero arguments. Either, it can take the path of the directory that needs to have it's contents listed as an argument. Or, in the case of no argument, the ls command simply lists the contents of the `cwd`.  In this scenario, the flag file inside the challenge directory was renamed, so we could use `ls /challenge` to list the contents of the challenge directory and find the new flag file and invoke it to find the flag.

```
hacker@commands~listing-files:~$ ls /challenge
27677-renamed-run-6055  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/27677-renamed-run-6055
Yahaha, you found me! Here is your flag:
pwn.college{EWwIJp2Wj1aZOABiaElNB9V-n1A.QX4IDO0wCMxAzNzEzW}
```

## What I Learned
I learnt the use of the `ls` command, which allows us to list all the contents of a directory, whether they be sub-directories or files of any type. Because of this command, we do not need to always remember the names of all files or their paths, as we can simply use the `ls` command to see if they exist in the directory or not.

## References
None.