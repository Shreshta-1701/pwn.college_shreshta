# Matching With *
The challenge asks you to open the terminal in the pwn.college DOJO and use `*` to keep the argument to cd at a minimum and get the flag.

## My Solve
**Flag:** `pwn.college{42Gp3sBIERzyir-AV1fWPjn-xQg.QXxIDO0wCMxAzNzEzW}`

File Globbing allows us to avoid having to write extremely long filepaths every time we wish to invoke a program or do anything with Linux really. This challenge teaches us the first globbing technique, which is `*`. Whenever the terminal sees the `*` character in association with what seems to be a path, this character is then replaced by a "wildcard", which is essentially the closest matching term to whatever you wrote before `*`. For example, if in this challenge directory, I had 3 sub-directories named files_a, folder_b, directory_c, and I wanted to cd into the `folder_b` directory, while being in `/home/hacker`, without writing out the entire filepath, then I would simply need to run, `cd /*/fo*`. Here, the asterix in front of 'fo' means that the process will check for the closest match to the search term, which is `folder_b` here, and the asterix before it, will automatically be replaced by `/challenge` as `folder_b` lies in that directory. In a similar way, in this challenge, we had to cd into the challenge directory before invoking the program to run the flag, but keep our argument to a maximum of 4 characters. So we execute `cd /ch*`.


```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{42Gp3sBIERzyir-AV1fWPjn-xQg.QXxIDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about the process of File Globbing and how we can use the `*` character to shorten our file paths without any hassle. I was also able to learn about all the different ways in which this globbing technique can be used, depending on the scenario.

## References
None.