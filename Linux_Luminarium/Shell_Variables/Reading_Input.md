# Reading Input
The challenge asks you to open the terminal in the pwn.college DOJO and store a value entered by the user in a variable.

## My Solve
**Flag:** `pwn.college{sA0Ed9B31EkbER1SXEIC6tZFC3W.QX4cTN0wCMxAzNzEzW}`

In this challenge, we learn how to take input from the user. This can be done with the `read` command, with its argument being the variable in which we want the value to be stored in. For example, `read PWN` stores the entered value in the PWN variable which can be accessed later. In this challenge, we are asked to read 'COLLEGE' into the PWN variable. Doing this gives us the flag.

```
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{sA0Ed9B31EkbER1SXEIC6tZFC3W.QX4cTN0wCMxAzNzEzW}
```

## What I Learned
I learnt how we can take input from the user and at the same time store this input in a variable which can be accessed at any point.

## References
None.