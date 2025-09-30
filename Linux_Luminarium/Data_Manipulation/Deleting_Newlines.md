# Deleting Newlines
The challenge asks you to open the terminal in the pwn.college DOJO and delete newline characters from the stdout.

## My Solve
**Flag:** `pwn.college{k0Dq_95kw7kdBW2-dS1XAlLm8fR.0VNxEzNxwCMxAzNzEzW}`

A common class of characters that we need to remove most of the time are line separators. For example, when printing out `echo hello_world`, if we wish to print out hello and world in different lines, we need to get rid of the invisible `\n` tag. For this, we execute `tr -d "\n"`. We must put the line separators inside `" "` as otherwise the shell would think of `\n` as characters to be replaced. For this challenge, we execute `/challenge/run | tr -d "\n"` to give us the flag.

```
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{k0Dq_95kw7kdBW2-dS1XAlLm8fR.0VNxEzNxwCMxAzNzEzW}
```

## What I Learned
I learnt about how we can delete newline separators from our standard outputs, which is a very common process when working with the shell.

## References
None.