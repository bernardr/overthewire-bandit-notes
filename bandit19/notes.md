Flag to enter: 

IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

n access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.


* * * * 

Thi was a little confusing as I thought I had to run `setuid` but apparently the `bandit20-do` binary _is_ the correct one. Cool. 

I ran `file` and `xxd` for kicks, but didnt generate much ineteresting info. 

* * * * 

## Solution: 

ran: 

`./bandit20-do cat /etc/bandit_pass/bandit20
` 

Flag = GbKksEFF4yrVs6il55v6gwY5aVje5f0j
