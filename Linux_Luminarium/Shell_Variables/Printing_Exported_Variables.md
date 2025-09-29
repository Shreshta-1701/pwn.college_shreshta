# Printing Exported Variables
The challenge asks you to open the terminal in the pwn.college DOJO and print all variables that have already been exported in the shell, to get the flag.

## My Solve
**Flag:** `pwn.college{4ja4HlNZB2Km36g7YILujXKggxC.QX4UTN0wCMxAzNzEzW}`

We already know that the `echo` command can be used to print the value inside a variable in the shell. However, there is another command which we can use to print out **ALL** variables that have been previously exported in the shell. This command is `env`. In this challenge, executing this command prints out many exported variables. Among these variables is the FLAG variable, with the flag value beside it.

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=7b4e75f746b086a6f8c228d5557f9388c3ef57ced7cddc97f2650bff7f934157
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{4ja4HlNZB2Km36g7YILujXKggxC.QX4UTN0wCMxAzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-kitty
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I Learned
I learnt how we can use the `env` command to print out all exported variables in the current shell process.

## References
None.