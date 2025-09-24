# Linking Files
The challenge asks you to open the terminal in the pwn.college DOJO and create a symbolic link between the flag file and another file to access it and get the flag.

## My Solve
**Flag:** `pwn.college{IHU3CPZ-s7TfgQcW404xU2Kv0Ws.QX5ETN1wCMxAzNzEzW}`

The `ln` command can be used to create links between files and directories. These links are especially useful when multiple files are meant to lead the user to the same location. You can either create a hard link or a soft link. A hard link actually makes the accesses of the original file and the linked file completely identical, whereas a soft link (or symbolic link) just links the contents of the original file to the linked one on execution. Soft links are more widely used as hard links have various disadvantages. We can create a soft link using `ln -s` and then entering the original file path, and then the link path. In this challenge, the `/challenge/catflag` file is linked to `~/not-the-flag`, which doesn't containt the flag, but `/flag` does. So we first remove the `~/not-the-flag` file, so that a new link can be formed from `/flag` to `~/not-the-flag`. Once the symbolic link is created, `/challenge/catflag` can be invoked again as it now links to `/flag` indirectly through `~/not-the-flag`, and now it gives us the flag.

```
hacker@commands~linking-files:~$ rm ~/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{IHU3CPZ-s7TfgQcW404xU2Kv0Ws.QX5ETN1wCMxAzNzEzW}
```

## What I Learned
I learnt how we can create links between files in Linux and about the differences between hard links and soft links and how both of them can be used. I was also able to learn that already linked files cannot be linked again, which is why I had to first remove `~/not-the-flag`. This command is extremely useful for huge workloads where you will have multiple programs and functions leading to the same final file or location, and now with our newly gained knowledge, we could simply create links to make our workflow more convenient.

## References
None.
