Flag to enter: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

* * * 

http://overthewire.org/wargames/bandit/bandit12.html

* * * * 

## Clue: 

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
Helpful Reading Material


* *  * *

Found the following as an example of how to do ROT13 in terminal: 

 tr '[A-Za-z]' '[N-ZA-Mn-za-m]'

Added `cat data.txt | ...` 

But also probably could have done it via the internet decoders out there. 

* * * 

The flag = 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

