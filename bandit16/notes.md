Flag to enter = cluFn7wTiGryunymYOu4RcffSxQluehd

* * * * 

http://overthewire.org/wargames/bandit/bandit17.html

## Clue

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap
Helpful Reading Material

    Port scanner on Wikipedia

* * * * 

Used the following nmap search: 

`nmap -A localhost -p 31000-32000 -vv`

We have these ports: 

Open ports: 

31046/tcp open  echo        syn-ack
31518/tcp open  ssl/echo    syn-ack
31691/tcp open  echo        syn-ack
31790/tcp open  ssl/unknown syn-ack
31960/tcp open  echo        syn-ack


Eliminating all of the other ports, able to single out `31790` for being SSL and meeting our requirements. 

Connect to `31790`: 

`openssl s_client -connect localhost:31790' 

Got Flag! 

Flag in this case is an RSA private key found in the bandit17.key file



