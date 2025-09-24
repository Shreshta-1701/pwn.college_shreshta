# An Epic Filesystem Quest
The challenge asks you to open the terminal in the pwn.college DOJO and find the flag file by navigating through directories using the commands we have learnt about so far.

## My Solve
**Flag:** `pwn.college{QX0DEAB5jwDw-bjBsZIf4le5Vft.QX5IDO0wCMxAzNzEzW}`

This challenge is a way to practice all that we have learnt so far. It is an extremely long fetch-quest, that asks you to keep finding the next clue by navigating to and opening different files, directories, etc. Our first clue was that the file was in the `/` directory. From that point onward, opening the files with names related to 'clue' or 'evidence' kept giving you more and more clues. I had to make proper use of the `ls`,`cd`,`ls -a` and `cat` commands to find the next file, following the rules specified by the previous clue.

```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
INFO  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat INFO
Congratulations, you found the clue!
The next clue is in: /var/cache
hacker@commands~an-epic-filesystem-quest:/$ cd /var/cache
hacker@commands~an-epic-filesystem-quest:/var/cache$ ls
EVIDENCE  apache2  apt  debconf  dictionaries-common  fontconfig  ldconfig  man  private  sympow
hacker@commands~an-epic-filesystem-quest:/var/cache$ cat EVIDENCE
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/Documentation/ABI/obsolete

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/var/cache$ cd /opt/linux/linux-5.4/Documentation/ABI/obsolete
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/ABI/obsolete$ ls
SNIPPET          sysfs-class-net-batman-adv  sysfs-driver-hid-roccat-arvo      sysfs-driver-hid-roccat-konepure  sysfs-driver-hid-roccat-pyra  sysfs-firmware-acpi
sysfs-bus-usb    sysfs-class-net-mesh        sysfs-driver-hid-roccat-isku      sysfs-driver-hid-roccat-kovaplus  sysfs-driver-hid-roccat-ryos  sysfs-gpio
sysfs-class-dax  sysfs-class-typec           sysfs-driver-hid-roccat-koneplus  sysfs-driver-hid-roccat-lua       sysfs-driver-hid-roccat-savu
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/ABI/obsolete$ cat SNIPPET
Tubular find!
The next clue is in: /opt/linux/linux-5.4/scripts/dtc

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/ABI/obsolete$ ls -a /opt/linux/linux-5.4/scripts/dtc
.   .SPOILER    Makefile      checks.c  dt_to_config  dtc-parser.y  dtc.h     fdtdump.c  fdtput.c    fstree.c          libfdt      srcpos.c  treesource.c          util.c  version_gen.h
..  .gitignore  Makefile.dtc  data.c    dtc-lexer.l   dtc.c         dtx_diff  fdtget.c   flattree.c  include-prefixes  livetree.c  srcpos.h  update-dtc-source.sh  util.h  yamltree.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/ABI/obsolete$ cat /opt/linux/linux-5.4/scripts/dtc/.SPOILER
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/mako-1.3.10.dist-info/licenses

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/ABI/obsolete$ cd /usr/local/lib/python3.8/dist-packages/mako-1.3.10.dist-info/licenses
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/mako-1.3.10.dist-info/licenses$ ls
LICENSE  SECRET
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/mako-1.3.10.dist-info/licenses$ cat SECRET
Yahaha, you found me!
The next clue is in: /usr/share/icons/Humanity/places/22

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/mako-1.3.10.dist-info/licenses$ cd /usr/share/icons/Humanity/places/22
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ ls
TRACE                                 folder-open.svg          folder-visiting.svg       gnome-fs-blockdev.svg            gnome-fs-trash-empty.svg                  mail-inbox.svg             stock_trash_full.svg
application-x-gnome-saved-search.svg  folder-pictures.svg      folder.svg                gnome-fs-bookmark-missing.svg    gnome-fs-trash-full.svg                   mail-outbox.svg            trashcan_empty.svg
bookmark-missing.svg                  folder-publicshare.svg   folder_download.svg       gnome-fs-desktop.svg             gnome-home.svg                            mail-sent.svg              trashcan_full.svg
desktop.svg                           folder-remote-ftp.svg    folder_home.svg           gnome-fs-directory.svg           gnome-main-menu.svg                       network-server.svg         user-desktop.svg
distributor-logo.svg                  folder-remote-nfs.svg    folder_images.svg         gnome-fs-ftp.svg                 gnome-mime-x-directory-nfs-server.svg     network-workgroup.svg      user-home.svg
edittrash.svg                         folder-remote-smb.svg    folder_pictures.svg       gnome-fs-home.svg                gnome-mime-x-directory-smb-server.svg     network_local.svg          user-images.svg
emptytrash.svg                        folder-remote-ssh.svg    folders-documents.svg     gnome-fs-network.svg             gnome-mime-x-directory-smb-share.svg      novell-button.svg          user-pictures.svg
folder-documents.svg                  folder-remote.svg        folders-downloads.svg     gnome-fs-nfs.svg                 gnome-mime-x-directory-smb-workgroup.svg  other-desktop.svg          user-share.svg
folder-download.svg                   folder-saved-search.svg  folders-music.svg         gnome-fs-server.svg              gnome-stock-trash-full.svg                redhat-network-server.svg  user-trash-full.svg
folder-downloads.svg                  folder-system.svg        folders-publicshare.svg   gnome-fs-share.svg               gnome-stock-trash.svg                     server.svg                 user-trash.svg
folder-home.svg                       folder-templates.svg     gnome-ccdesktop.svg       gnome-fs-smb.svg                 gtk-directory.svg                         start-here.svg             xfce-trash_empty.svg
folder-images.svg                     folder-video.svg         gnome-desktop-config.svg  gnome-fs-ssh.svg                 gtk-network.svg                           stock_folder.svg           xfce-trash_full.svg
folder-music.svg                      folder-videos.svg        gnome-folder.svg          gnome-fs-trash-empty-accept.svg  inode-directory.svg                       stock_music-library.svg
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ cat TRACE
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/arch/csky/include/uapi/asm
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ ls -a /opt/linux/linux-5.4/arch/csky/include/uapi/asm
.  ..  GIST  Kbuild  byteorder.h  cachectl.h  perf_regs.h  ptrace.h  sigcontext.h  unistd.h
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ cat /opt/linux/linux-5.4/arch/csky/include/uapi/asm/GIST
Congratulations, you found the clue!
The next clue is in: /usr/lib/R/library/tcltk/R

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ ls /usr/lib/R/library/tcltk/R
HINT-TRAPPED  tcltk  tcltk.rdb  tcltk.rdx
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ cat /usr/lib/R/library/tcltk/R/HINT-TRAPPED
Great sleuthing!
The next clue is in: /usr/include/gio-unix-2.0/gio

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ ls -a /usr/include/gio-unix-2.0/gio
.   ALERT-TRAPPED      gfiledescriptorbased.h  gunixcredentialsmessage.h  gunixfdmessage.h    gunixmounts.h        gunixsocketaddress.h
..  gdesktopappinfo.h  gunixconnection.h       gunixfdlist.h              gunixinputstream.h  gunixoutputstream.h
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Humanity/places/22$ cat /usr/include/gio-unix-2.0/gio/ALERT-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{QX0DEAB5jwDw-bjBsZIf4le5Vft.QX5IDO0wCMxAzNzEzW}
```

## What I Learned
I was able to put to use all the knowledge that I have gained so far in this Linux module, and navigate through multiple directories, all while following rules specified by clues, to finally find the flag at the end.

## References
None.
