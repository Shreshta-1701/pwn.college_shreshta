# Grepping
The challenge asks you to open the terminal in the pwn.college DOJO and search the contents of the 'data.txt' file to find the flag text hidden within it.

## My Solve
**Flag:** `pwn.college{kf7yALHjJCPnvs_Ri-pkSudSkH9.QX3EDO0wCMxAzNzEzW}`

In this challenge, we learn how to search through the contents of a file using the `grep` command. The `grep` command takes 2 arguments. First is the string that we want to search for. Over here, the flags always start with 'pwn.college', hence making that our search string. The 2nd argument is the path to the file in which we want this search to be carried out. Hence, making the command in our case `grep pwn.college /challenge/data.txt`.

```
hacker@commands"grepping-for-a-needle-in-a-haystack: ~$ grep pwn.college /challenge/data.txt

pwn.college{kf7yALHjJCPnvs_Ri-pkSudSkH9.QX3EDO0wCMxAzNzEzW}
```

## What I Learned
I learnt about the `grep` command and how we can use it to search for some text within a specified file, allowing us to search the contents of a large file without having to do it manually.

## References
None.