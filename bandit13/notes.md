Flag to enter: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL


* * * * 

http://overthewire.org/wargames/bandit/bandit14.html

## Clue 

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on
Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap
Helpful Reading Material

    SSH/OpenSSH/Keys


* * * * * 

Fuck yea! 


First, use cat to read the new key. Copy and paste that key locally. 

Leave the session.

Change permissions on the new key with: 

`chmod 600 KEYNAME` 

then login via ssh: 

`ssh -i NEWFILE bandit14@...` 

Key = 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e


