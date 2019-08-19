Flag to enter = bandit17.key 

Entered with the following command: 

`ssh i- BANDIT.KEY banditUSERNAME@BANDITSERVER -p 2220` 

* * * * 

### Clue: 

Level Goal

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19


* * * * 

Potential solution: 

`diff passwords.old passwords.new`

Possible FLag: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd


WORKED! 

Flag = kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd



