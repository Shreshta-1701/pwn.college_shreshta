# Named Pipes
The challenge asks you to open the terminal in the pwn.college DOJO and create a persistent named pipe.

## My Solve
**Flag:** `pwn.college{ApPCyMGvDTE6-IrYBI6TtZjKbfZ.01MzMDOxwCMxAzNzEzW}`

In this challenge, we are tasked with creating a `/tmp/flag_fifo` file, which is a persistent named pipe file or a `FIFO`. We can do this by using the `mkfifo` command, which takes the argument as the path of the file to be created. One important thing to remember about FIFO's is that, while they are more useful, they are also more difficult to use, as they blcok actions and operations on them until both their read and write sides are open. So when working with FIFO's, you will most likely have to use multiple shell process just to continue operating on them. Similary, here, we execute `mkfifo /tmp/flag_fifo` to make a FIFO or persistent named pipe with the name `/flag_fifo` inside `/tmp`. After this, we execute `/challenge/run > /tmp/flag_fifo`, which redirects the output of the run program to the FIFO. Now, since a FIFO blocks further actions until both its read and write sides are open, and currently only its write side is open, therefore it won't let us do anything else in this shell process and we must create a new one. In this new process, we execute the command `cat /tmp/flag_fifo` to read the FIFO and get the flag. After this, the original shell process is also freed up.


```
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
<In new shell process>
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{ApPCyMGvDTE6-IrYBI6TtZjKbfZ.01MzMDOxwCMxAzNzEzW}
```


## What I Learned
In this challenge I learnt about FIFO's and their advantages and disadvantages and how we can operate on them and make them in the first place.

## References
None.