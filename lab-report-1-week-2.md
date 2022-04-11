# **Week 2 Lab Report**
---
## 1. Installing VScode

Installing VScode from their website and follow their download instructions.

![Image](./Screen%20Shot%202022-04-10%20at%201.19.32%20AM.png)
* the application should open to this page.
---
## 2. Remotely Connecting

To remotely connect to a computer, open a new terminal and write this command:

> `ssh [username]@ieng6.ucsd.edu`

Type **yes** if logging in for the first time, as it will ask for a confirmation.

![Image](./Screen%20Shot%202022-04-10%20at%204.36.56%20PM.png)
* If the password is properly entered and has successfully logged in, the output should look like this.
---
## 3. Trying Some Commands

After logging into the remote computer, you can try some commands:

* `cd ~`
* `cd`
* `ls -lat`
* `ls <directory>` where `<directory>` is `/home/linux/ieng6/cs15lsp22/cs15lsp22abc` and `abc` is a username
* `cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/`
* `cat /home/linux/ieng6/cs15lsp22/public/hello.txt`

![Image](./Screen%20Shot%202022-04-10%20at%205.12.02%20PM.png)
* when running the commands correctly, the output should look somethinng like this.
---
## 4. Moving Files with `scp`

To move files from local and remote computers, `scp` is used.

As an example, I will be moving a file called WhereAmI.java from my computer to a remote computer.

> tip: Make sure to check if you are in the correct directory

![Image](./Screen%20Shot%202022-04-10%20at%205.27.33%20PM.png)
* This is what shows up when running the file.
> Note: there shouldn't be the WhereAmI.class, since this was a screenshot after I put the file in the remote computer.

Then we run this command through `scp`:

`scp [File Name].java [Username]@ieng6.ucsd.edu:~/`
![Image](./Screen%20Shot%202022-04-10%20at%205.38.07%20PM.png)
* This is what shows up when running the command.

Then log back into ssh and run the `ls` command.
![Image](./Screen%20Shot%202022-04-10%20at%205.53.57%20PM.png)
* This should be what the command should result in, with the WhereAmI.java file in the remote computer.
---
## 5. Setting an SSH Key

To avoid the time consuming process of typing in a password to log into scp, we can use `ssh` keys.

We use `ssh-keygen` to create a public key and a private key to use in place of one's password.

First we make sure we are on our computer. Then we run this following command:

> `ssh-keygen`

Then make sure to **not** add a passphrase, and procceed to press enter twice.

![Image](./Screen%20Shot%202022-04-10%20at%206.06.14%20PM.png)
* The outcome should look something like this.

Now to copy the public key to the .ssh directory of the server enter in these commands:

> `$ ssh [Username]@ieng6.ucsd.edu`

> `$ mmkdir .ssh`

> `$ exit`

After logging out go back to the client and enter this command:

> `$ scp /Users/<user-name>/.ssh/id_rsa.pub [User name]@ieng6.ucsd.edu:~/.ssh/authorized_keys`

Now you are able to `ssh` or `scp` without entering in a password.

---
## 6. Optimizing Remote Running

To make remote running more efficient, here are some tips to more efficiently copy files to the remote server and running it.

To check the directory on the remote server, use this command to save time:

> `ssh [User name]@ieng6.ucsd.edu "ls"`

![Image](./Screen%20Shot%202022-04-10%20at%206.33.41%20PM.png)
* When run successfully, this is what the output should look like.

You can also use semicolons to run a lot of commands in one line.

![Image](./Screen%20Shot%202022-04-10%20at%206.34.03%20PM.png)
* This is an example of many commands running on one line.