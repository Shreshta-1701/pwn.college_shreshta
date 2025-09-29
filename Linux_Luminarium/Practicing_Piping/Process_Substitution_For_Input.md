# Process Substitution For Input
The challenge asks you to open the terminal in the pwn.college DOJO and compare two command outputs.

## My Solve
**Flag:** `pwn.college{YJdqXiCfIyGT5_1adLOr0fpGWPN.0lNwMDOxwCMxAzNzEzW}`

We know that to compare files we can use the `diff` command. But it is not necessary to redirect the output of each command to an output file first so that we can use the `diff` command. Instead we can simply hook the input and output of programs to the arguments of commands, which can be done by Process Substitution. For reading from a command, we can use the following syntax - `<(command)`. Doing this will make bash run the command and hook up its output to a temporary file. This imaginary, temporary file is known as a **named pipe**, as it has a file name. Now, to compare two command outputs without having to create two different output files, we can simply execute `diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)`, which gives us the difference between the two files, where they are full of decoys, but the second file has an additional line which includes the flag.


```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
42a43
> pwn.college{YJdqXiCfIyGT5_1adLOr0fpGWPN.0lNwMDOxwCMxAzNzEzW}
```


## What I Learned
In this challenge I learnt how we can use Process Substitution to create temporary files or `named pipes` which can be used to operate on command outputs without having to create permanent output files, and I also learnt the syntax for reading from a command (Input Process Substitution).

## References
None.