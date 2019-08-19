Flag to enter: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

The Clue: 

> The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.
Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

* * * 

Niiice! used `strings` in order to read the `.data` file. Also usd `file` to read the type of file it is. 


Found a section that read "the password is..." 

* * *  *

Flag = truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
