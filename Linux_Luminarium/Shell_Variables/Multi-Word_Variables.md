# Multi-Word Variables
The challenge asks you to open the terminal in the pwn.college DOJO and then set a variable to a value containing multiple words.

## My Solve
**Flag:** `pwn.college{YXz8MA42w2J_R50V70wVqOwL98L.QXwYTN0wCMxAzNzEzW}`

In the previous challenge, we learned about how we can use `=` to assign values to variables. However, if we wish to assign values containing multiple words to a variable, simply executing statements like `PWN=COLLEGE YEAH` won't work. This works on the same principle as the rule that there should be no space around `=`. When we execute the aforementioned statement, the shell treats `YEAH` as a command. Hence, to assing multiple words to a variable, like in this challenge, we must enter something like `PWN="COLLEGE YEAH"`, in the case of this challenge. This gives us the flag.


```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YXz8MA42w2J_R50V70wVqOwL98L.QXwYTN0wCMxAzNzEzW}
```


## What I Learned
I learnt how to set a value of multiple words to a single variable, and why we cannot simply add on words without also having to use `""`.

## References
None.