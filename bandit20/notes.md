Flag to enter = GbKksEFF4yrVs6il55v6gwY5aVje5f0j

* * * *

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think
Commands you may need to solve this level

ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …) 


* * * * 

Wasted a lot of time doing an nmap read on open ports. 

Also wasted time reading up on background proceesses. :/ 


**Found this**: https://explainshell.com/explain?cmd=nc+-lvnp+4444

which explains the flags as: 

-l = listen 
-v = verbose 
-n = numeric only, no DNS
-p = port 


The good news is that I eventually figured out (and googled a little :/) that I should create a second session. 


In the first session. Setup a netcat listener on any port:

`nc -l -lvnp 1234` 


In a second terminal session, login to bandit20. In the second session run the binary. `/suconnect` on port 1234. 

You'll now have a device connected in the first session. Now, enter the password for the Bandit 20 - `GbKksEFF4yrVs6il55v6gwY5aVje5f0j`. 


THis will give you a read input in the second session and output the new password in the first. 

Flag = gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr



