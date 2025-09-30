# Extracting Specific Sections Of Text
The challenge asks you to open the terminal in the pwn.college DOJO and extract columns using the `cut` command.

## My Solve
**Flag:** `pwn.college{cQZfg0nPuTP7qY1TMRZZGLyDpE_.01NxEzNxwCMxAzNzEzW}`

Another useful command when it comes to extracting data is `cut`. This command can be used to **cut out** and extract columns of data from our standard outputs. It takes multiple arguments. The first is the column delimiter or `-d`, whose value attached is the character that separates different columns, this character typically being a whitespace. After this, is the field number `-f`, whose value attached is the number of the column that we wish to print out. For this challenge, we had to run `/challenge/run`, cut out the 2nd column (the one which contains the flag), and then use `tr -d "\n"` to join all of them together into a single line. This makes the final command to be executed - `/challenge/run | cut -d " " -f 2 | tr -d "\n"`.

```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{cQZfg0nPuTP7qY1TMRZZGLyDpE_.01NxEzNxwCMxAzNzEzW}
```

## What I Learned
I learnt about how we can use the `cut` command to extract specific columns of text from documents and how it's arguments and values work.

## References
None.