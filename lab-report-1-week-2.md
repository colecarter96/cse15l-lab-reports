Lab Report 1
===

Step 1 (Downloading VS Code)
---
First, click [VS Code download for Mac](https://code.visualstudio.com/) and click the download button in the top right.
![Image](screenshots/Screen%20Shot%202022-04-08%20at%205.32.50%20PM.png)
Once you do this, unzip the file and finish the install like normal for downloading Mac apps.

Step 2 (Remotely Connecting)
---
* When remote connecting you must create a **New File** in VS Code. Once you do this write some code in the file and save it under a name. 
* Now go to this link, [Remote Username](https://sdacs.ucsd.edu/~icc/index.php), to find your username and password reset using the change your password link after clicking on your username button. 
![Image](screenshots/Screen%20Shot%202022-04-08%20at%205.45.19%20PM.png)

* Now you can go back to VS Code and go to the terminal and type (<username> will be your username that is found on the linked webpage):

    `$ ssh <username>@ieng6.ucsd.edu`

    this will prompt you for a password in which you can type in your password. After reseting your password using the "change your password" link on the page, it can take up to 15 minutes for your password change to go into effect. When typing in your password it will not show you the characters for security. Once you succesfully type your password you will be connected and some information about the remote computer will be given as shown below.
    ![Image](screenshots/Screen%20Shot%202022-04-09%20at%206.05.22%20PM.png)

Step 3 (Commands to run)
---
Now that you have connected to the remote server there are many commands that you can run. Some tha you can run are listed here:
```
$ cd ~
$ cd
$ ls
$ pwd
$ cat
```
These commands can be used to gain important information about the directory you're in, file you want to access, or the file you want to print. It may look something like this when you run it.

![Image](screenshots/Screen%20Shot%202022-04-09%20at%206.45.17%20PM.png)

Step 4 (Copying Files from Client to Server)
---
One useful thing that you can do when connected to the remote server is copy a file from your computer to the remote server. You can do this by running this command:

`scp "FileName" "username"@ieng6.ucsd.edu:~/`

This will prompt you for a password and then copy the file to the server computer. If you now run ls it will show the file that you copied to the server.

Step 5 (Making keys using Keygen)
---

For this step there are a list of moves to create keys using keygen.

* `$ ssh-keygen`
* You should see `Generating public/private rsa key pair`
* Next you should see `Enter file in which to save the key`
* You will write `(/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa`
* Then `Enter same paraphrase again:` will be shown in which you click enter and again when it says to enter again
* It will tell you the key and give you the unique randomart image
* Next on the server type the command `$ mkdir .ssh`
* You can now logout by typing `$ exit` 
* Back on your computer type the command `$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys`

You can now connect to the server without inputting a password.

Step 6 (Running Commands More Efficiently)
---

When trying to run commands on the remote server it can seem like a lot of typing. There are some ways to make it much more efficient. One way to to do this is running a command on the from your computer directly to the remote computer.

`ssh <username>@ieng6.ucsd.edu "ls"`

The command above would run the command on the server and then exit. You can also string commands together using semicolons.

`cp Main.java; javac Main.java; java Main`

Finally if you have a command that you previously called that you want to cal again you can use the up arrow to get previously used commands.

