Week 6 Lab Report
===

Written by Cole Carter
---


Part 1 Stremlining ssh Configuration
---

* This is what my config file looks like with my ssh login in. You can find this by doing ```cd ~/.ssh``` in a terminal and then ```pwd``` in order to have the directory pop up. Finally if you command + click this it will open the config file. It should look something like this:

    ![Image](screenshots/Screen%20Shot%202022-05-08%20at%207.27.21%20PM.png)

* You can create an alias using next to where it says "Host". Now that I have created my alias I can log in to the reomte server through the alias like this

You can see I type   ```ssh ieng6```  and I'm able to log in using my alais, which is ieng6

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%209.02.22%20AM.png)



* Here I used the touch command to create that new file ```random.txt``` and then I used scp to copy it to the remote server:

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%2011.08.37%20PM.png)


Part 2 Github Access From ieng6
---

* First we can add our key to github in the settings, once added it looks like this

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%209.16.19%20AM.png)

* Next if you type these commands in the terminal you can find where the key is stored.

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%203.52.38%20PM.png)


* Using this remote key on Github it is possible to login to the remote server and change the repo. Once the change is made, it is then possible to commit and push to the Github Repo online, as seen below

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%2010.37.16%20PM.png)

Part 3 Copy Whole Directories With ```scp -r```
---


* Now that the alias is set up there are commands that copy whole directories to the remote server. One is 
```scp -r . <alias>:<file>```

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%209.10.20%20AM.png)

* Now the whole markdown-parser has been copied to the remote server. Once in the remote server you can run the commands that run the tests in the repo like this:

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%2010.47.50%20PM.png)

* You can combine those two into one line using a semicolon and then the tests will run like this:
 
    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%2011.00.19%20PM.png)


* Or from your local client you can combine all of the steps into one line that looks like this: 

    ```scp -r . ieng6:markdown-parse ; javac -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java ; java -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest```

* And the output looks like this:

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%2011.04.17%20PM.png)

    ![Image](screenshots/Screen%20Shot%202022-05-16%20at%2011.04.25%20PM.png)