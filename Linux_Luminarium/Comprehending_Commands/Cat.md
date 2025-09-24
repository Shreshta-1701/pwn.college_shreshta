# Cat
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the cat command to read the flag file.

## My Solve
**Flag:** `pwn.college{k5rFPNM_2Afzqk6MLNMeaQMoyg1.QXxcTN0wCMxAzNzEzW}`

The `cat` command can be used to read any file within the terminal itself. It can take multiple arguments and concatenates the files together in such a scenario. If there is no argument, then cat will read from the terminal's input and output. The command allows us to quickly look at the contents of any file without having to open it in a specific software. Here, we can use `cat ./flag` to ask the cat command to read the flag file within the home directory, or cwd, which is why we use `./`.


```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat ./flag 
pwn.college{k5rFPNM_2Afzqk6MLNMeaQMoyg1.QXxcTN0wCMxAzNzEzW}
```


## What I Learned
I learnt about the `cat` command and how it can be used to read files and different files right within the terminal, even being able to concatenate multiple files together.

## References
None.