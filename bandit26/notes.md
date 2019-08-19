Entry Flag = uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG 

Ok, super weird one.

Loggging in via bandit 25 with the bandit26 ssh key should start us off. 

`bandit -i bandit26.sshkey localhost` 

will get us into the machine, *but* we get immediately logged out because a script executes. 

The script is running `more` .... which is a little like `less` *except* that you can run commands in it. Which is what we're going to do. 

**First** open a new window and resize so its small. Then log in. 

From here, if we press `v` we can see the banner in VIM. 

VIM allows us to read files and execute commands so, in order to grab a shell, we can simply enter the following in vim: 

(hit `escape` to enter into command mode) 

`:set shell /bin/bash`

then 

`:shell`

Boom. 

This should pop us in the bandit26 shell. 

* * * * 

Now, to get the bandit27 flag. 

We run bandit27-do executable and have it read the password file. 

`./bandit27-do cat /etc/bandit_pass/bandit27`

and we get our flag. 

Flag = 3ba3118a22e93127a4ed485be72ef5ea
