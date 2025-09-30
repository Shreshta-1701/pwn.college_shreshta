# Sorting Data
The challenge asks you to open the terminal in the pwn.college DOJO and sort an stdout alphabetically.

## My Solve
**Flag:** `pwn.college{AtlJ8ozm8hnkltWUwb1J4pxrGbw.0FM0MDOxwCMxAzNzEzW}`

The output lines of a command may not always be in our desired order. However, we can use the `sort` command in order to organize them. This command reads lines from the input (our stdout file in this case) and outputs them in a sorted order. By default, it sorts lines alphabetically, however, we can also sort them in other ways with different arguments like `-r`,`-n`,`-u`,`-R`, etc. which stand for `reverse order`, `numeric sort`, `unique lines only`, and `random order` respectively. For this challenge, we needed to find the flag from the file `/challenge/flags.txt`. We have also been told that when sorted alphabetically, flags.txt would contain the flag at the very end of the file. Hence, we know that sorting the file in reverse order would cause the flag to be in the beginning. Hence, we execute the following command - `sort -r /challenge/flags.txt | head -n 1`, where the first half sorts the file in reverse alphabetical order, and the second half (after the pipe) extracts the first sentence from the new sorted file. This gives us the flag.

```
hacker@data~sorting-data:~$ sort -r /challenge/flags.txt | head -n 1
pwn.college{AtlJ8ozm8hnkltWUwb1J4pxrGbw.0FM0MDOxwCMxAzNzEzW}
```

## What I Learned
I learnt about how we can use the `sort` command to sort data according to our liking in files.

## References
None.