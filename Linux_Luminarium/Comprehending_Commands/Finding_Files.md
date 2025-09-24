# Finding Files
The challenge asks you to open the terminal in the pwn.college DOJO and find the flag file within the root directory with the help of commands.

## My Solve
**Flag:** `pwn.college{8XK0CDdR1-uw6F3cKh5RlRxvCOC.QXxMDO0wCMxAzNzEzW}`

We can use the `find` command to find any file in any directory. However, there are multiple ways to use this command. It can take 2 types of argument. The first, is the path of where you wish to search for this file. This can be left empty as well, if one wishes to search the `cwd` of the terminal process. The other argument it can take is the search criteria for the file. For example, we can use the `-name` critera and specify a string from the name of the file that we wish to find. This makes searching for files much faster. Typically, one should make use of both arguments so that the `find` command gives you the desired output quickly, but in case you do not know where the file is located, or the exact name of the file, we can still use the command while omitting some of the arguments. In this challenge, the name of the file to be found is `flag`, and it exists somewhere in the system. So we run `find / -name flag` to search for files with the name `flag` within the `/` or root directory. We do not have the ability to access some directories, and hence for them, the process displays an error, but it still keeps running. The flag is also not found in the very first file named `flag` as there are multiple files with the same name on the system. The actual flag for this scenario is found in the second file found, and we can use `cat` to read its contents and get the flag. 

```
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
.
.
.
/opt/pwndbg/.venv/lib/python3.8/site-packages/elftools/common/__pycache__/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
.
.
.
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /opt/pwndbg/.venv/lib/python3.8/site-packages/elftools/common/__pycache__/flag
pwn.college{4K8S5iNJS7x24uDZ3PUjjSNfIeh.QXyMDO0wCMxAzNzEzW}
```

## What I Learned
I was able to learn how we can use the `find` command in Linux to find any file in any directory. I also learnt how we can omit different arguments from the command depending on what information we already have about the file to be found. In a way, it works similarly to the `grep` command which searches through the contents of a file for a specified string. Only here, this process is carried out on a much larger scale and is used to locate files instead of the contents of a file.

## References
None.
