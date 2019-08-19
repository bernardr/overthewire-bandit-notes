Flag to enter = kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

* * * * 

## Clue 


The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.


* * * *  

Entered w/ the following: 

`ssh bandit18@bandit.labs.overthewire.org -p 2220 -n cat readme`

This the `-n` flag allowed me to create execute a command without having a shell on the machine. In this case it was `cat`. 

This from the man page of `ssh` was helpful: 

> A common trick is to use this
             to run X11 programs on a remote machine.  For example, ssh -n shadows.cs.hut.fi
             emacs & will start an emacs on shadows.cs.hut.fi, and the X11 connection will
             be automatically forwarded over an encrypted channel.  The ssh program will be
             put in the background.  (This does not work if ssh needs to ask for a password
             or passphrase; see also the -f option.)


* * * * 

Flag = IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

