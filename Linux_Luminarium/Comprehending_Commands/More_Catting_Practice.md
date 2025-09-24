# More Catting Practice
The challenge asks you to open the terminal in the pwn.college DOJO and read the flag file in a deeply hidden directory using the `cat` command.

## My Solve
**Flag:** `pwn.college{8xbwKG5qtzqfJJr2aiLvIIOJ5-1.QXwITO0wCMxAzNzEzW}`

This challenge is an extension of the previous ones, where we need to use the cat command with an absolute path to read the flag file and find the flag. The only difference here is that the flag is located in a much deeper sub-directory.

```
You cannot use the 'cd' command in this level, and must retrieve the flag by absolute path. Plus, I hid the flag in a different directory! You can find it in the file /lib/jvm/java-1.11.0-openjdk-amd64/flag. Go cat it out **without** cding into that directory!

hacker@commands~more-catting-practice:~$ cat /lib/jvm/java-1.11.0-openjdk-amd64/flag

pwn.college{8xbwKG5qtzqfJJr2aiLvIIOJ5-1.QXwITO0wCMxAzNzEzW}
```

## What I Learned
I was able to further apply my knowledge of the `cat` command to access the flag file hidden in a deep sub-directory, allowing me to read the file and find the flag.

## References
None.