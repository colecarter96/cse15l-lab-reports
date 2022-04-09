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

    this will prompt you for a password in which you can type in your password. After reseting your password using the "change your password" link on the page, it can take up to 15 minutes for your password change to go into effect. When typing in your password it will not show you the characters for security. Once you succesfully type your password you will be connected and some information about the remote computer will be given.
