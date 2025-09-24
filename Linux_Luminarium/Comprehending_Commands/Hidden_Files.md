# Hidden Files
The challenge asks you to open the terminal in the pwn.college DOJO and find the name of the hidden flag file in a directory using a variation of the `ls` command.

## My Solve
**Flag:** `pwn.college{YfLdH-goQDEEPilkfWWiX-n50Fn.QXwUDO0wCMxAzNzEzW}`

The `ls` command in Linux doesn't list all files and directories by default. Some files and directories are **hidden**, not to be found normally. These files are known as **dotfiles**, for their names always start with a dot. We can however, use a variation of the ls command to list all files and directories (including hidden ones) at the specified path in the argument of the ls command. For this, we must use `ls -a`, which lists all the contents of a directory. Hence, over here, we must run the command `ls -a /` to list all the contents of the root directory. Here we can find a file named `.flag-14955260288717` which had been hidden. Now we can use the `cat` command to display the contents of the file, as we know its name. This gives us the flag.

```
hacker@commands~hidden-files:/$ ls -a /
.  ..  .dockerenv  .flag-14955260288717  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~hidden-files:/$ cat /.flag-14955260288717
pwn.college{YfLdH-goQDEEPilkfWWiX-n50Fn.QXwUDO0wCMxAzNzEzW}
```

## What I Learned
I learnt that Linux can have hidden files and directories known as `dotfiles` that are not normally displayed in file explorers, or even in the terminal when using commands such as `ls`. I was also able to learn a way to bypass this security measure, as using the `ls` command with `-a` allows the terminal to list all the contents of the specified directory, including hidden files.

## References
None.
