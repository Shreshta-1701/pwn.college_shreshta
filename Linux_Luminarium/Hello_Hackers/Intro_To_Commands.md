# Intro To Commands
The challenge asks you to open the terminal in the pwn.college DOJO and invoke commands to print the username and also to get the flag.

## My Solve
**Flag:** 'pwn.college{0hQojBSPWXLw6T8-oxHJVMnzYz1.QX3YjM1wCMxAzNzEzW}'

First we execute the 'whoami' command in the terminal, which displays the current user's name in the terminal. We are currently operating as the 'hacker' user, which is why each line of the terminal starts with 'hacker@hello~intro-to-commands:~$'

Next, we can use the 'hello' command which gives us the flag in return.

'''bash
hacker@hello~intro-to-commands:~$ whoami
hacker
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{0hQojBSPWXLw6T8-oxHJVMnzYz1.QX3YjM1wCMxAzNzEzW}'''

## What I Learned
I was able to learn about linux commands such as 'whoami' and how to use the terminal to operate in a Unix based environment, all of which will be very useful in the later challenges of the course. I also learned that Linux Commands are Case-Sensitive, and hence, 'HELLO' and 'hello' are entirely different commands.

## References
None.