
Flag to next directory: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs


find directory-location -group {group-name} -name {file-name}

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

* * * * 

So this doesn't really make much sense, I was able to the flag via the same guy as before:  

https://medium.com/@Kan1shka9/overthewire-wargames-bandit-walkthrough-df2b86826c67

here's the solution command: 

`find / -user bandit7 -group bandit6 -size 33c 2>/dev/null` 

* * * *

What's weird about thsi is the first part of the command makes lots of sense. The weird part is tail of command: 



`2>/dev/null` 


* * * * 

I found this answer via StackOver flow: https://askubuntu.com/questions/350208/what-does-2-dev-null-mean


The > operator redirects the output usually to a file but it can be to a device. You can also use >> to append.

If you don't specify a number then the standard output stream is assumed but you can also redirect errors

> file redirects stdout to file
1> file redirects stdout to file
2> file redirects stderr to file
&> file redirects stdout and stderr to file

/dev/null is the null device it takes any input you want and throws it away. It can be used to suppress any output.


