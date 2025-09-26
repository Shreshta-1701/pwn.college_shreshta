# Searching Manuals
The challenge asks you to open the terminal in the pwn.college DOJO and pass the correct argument to the challenge program to find the flag by seaching for it in the documentation.

## My Solve
**Flag:** `pwn.college{QZ64e0KFmqqa84cLvkhg20WTi05.QX1EDO0wCMxAzNzEzW}`

In this challenge, we further explore how we can utilize the full potential of the `man` command. If the documentation for any command is extremely long, then it could make the process of figuring out the correct arguments very tedious. But Linux also allows us to search through the manual for a command. By pressing the `/` key while having the manual opened, we can enter a search term. After this, we can navigate through the matching terms with `n` to go forward and `N` to go backwards. In this challenge, by searching the manual for the challenge command with `/flag`, and by going forward a few matches, we found the `--mhjh` argument, which had been stated to give us the flag. Hence, we simply entered `/challenge/challenge --mhjh` to get the flag.

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --mhjh
Initializing...
Correct usage! Your flag: pwn.college{QZ64e0KFmqqa84cLvkhg20WTi05.QX1EDO0wCMxAzNzEzW}
```


## What I Learned
I learnt about how we can search for specific arguments or terms in the documentation for any command to make our learning journey easier, allowing us to skip the tedious task of navigating through extremely long documentation when searching for the description of a single argument.

## References
None.