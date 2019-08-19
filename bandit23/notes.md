Entry flag = jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n 

* * * * 

Clue: 

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around… 

* * * * 

I was on the right track for a small period of time but a few things fucked me up. Mostly the folder permissions. Here goes the expaliner: 


1 - Nav to /etc/cron.d/cronjob_bandit24 

2 - read the file: which runs this script: /usr/bin/cron_job24.sh

3 - Reading that script tells us that the cron script runs every minute. wiping files after its done. That's what the `* * * * ` is. 
4 -  We need to make our own sript. 

We create a temp directory. Here's one: `mkdir /tmp/tempdir` 

cd into that directory and create a script.sh file. Here's what the script should say "read the password file and write it to our temp folder". 

Here's the actual script: 

cat etc/bandit_pass/bandit24 > /tmp/tempdir/newpass.txt

We can also just use `cp` instead of cat. 

IMPORTANT: Change the permission of the file to be global: 

`chmod 777 script.sh` 

Finally, move the script to where the scripts are run. `/var/spool/bandit24/`. 

The script should be running every minute. So hit `date` for a count down, or wait. Then hit `ls` in our /tmp/tempdir folder. 

And here you go: 

Flag = UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 

This was insanely helpful: 

https://www.youtube.com/watch?v=gvW1zG6lvE8
