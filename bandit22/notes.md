entry Flag = Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI


* * * *  *

wow. This got kinda out of hand. 

Here's the methodology: 

First, navigate to `/etc/cron.d/` and find the relevant crontab file. In this case it's `cronjob_bandit23.sh`. 

Reading the file we can see the following: 

#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget


So we change `whoami` to `bandit23` and enter via the shell: 

`echo I am user bandit23 | md5sum | cut -d ' ' -f 1` 

this will give us the following md5 hash: 

8ca319486bfbbc3663ea0fbe81326349

This hash is the name of the foder located at /tmp/8ca319486bfbbc3663ea0fbe81326349

Doing a `cat` of that folder will produce our flag. 

Flag = jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
