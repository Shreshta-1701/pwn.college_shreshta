# Exporting Variables
The challenge asks you to open the terminal in the pwn.college DOJO and then set a variable to a value containing multiple words.

## My Solve
**Flag:** `pwn.college{MF05cYCwzQMVZJ6lVufaLN94NHt.QXyYTN0wCMxAzNzEzW}`

This challenge tells us about how whenever we set variables in a shell session, they won't carry over to the next one, and are local to that specific shell process. This is done so that variables which contain sensitive data don't leak over to other programs unless explicitly asked to do so. In order to explicitly ask the shell to do this, we must export our variables. This can be done by executing the `export VAR` command where VAR is the variable to be exported. Now, any child shells will be able to access the VAR variable and use it's value. We can also combine the `export` line with the line where we set values to the variable. 


```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{MF05cYCwzQMVZJ6lVufaLN94NHt.QXyYTN0wCMxAzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```


## What I Learned
I learnt how we can export variables to child shells so that other programs can access these variables and their values.

## References
None.