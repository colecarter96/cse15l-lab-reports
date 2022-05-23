Week 8 Lab Report
===

Written by Cole Carter
---


Snippet 1
---

* This is how the code was turned into a test using the implementation of MarkdownParse.java that I created.
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.50.53%20PM.png)

* This is the output for this test:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.39.04%20PM.png)

* This is the code for the test of the code that I reviewed in lab:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.50.35%20PM.png)

* This is the failure message:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.48.33%20PM.png)


Snippet 2
---

* This is the test for snippet two in my code implementation:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.51.03%20PM.png)

* This is the failure output:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.39.17%20PM.png)

* This is the test for snippet two of the code I reviewed:
![Image](screenshots//Screen%20Shot%202022-05-22%20at%2010.50.35%20PM.png)

* This is the failure output:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.48.53%20PM.png)


Snippet 3
---

* This is the code for the snippet 3 test on my implementation:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.51.11%20PM.png)

* This is the failure output:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.39.34%20PM.png)

* This is the test for snippet three of the code I reviewed:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.50.35%20PM.png)

* This is the failure output:
![Image](screenshots/Screen%20Shot%202022-05-22%20at%2010.49.03%20PM.png)


Fixing Snippet 1
---

 I __think__ when it comes looking for the code with backticks I think you could accomplish this through doing an if statement after checking for backticks and ensure that they aren't in a position that would cause a link to be invalid. This could be as easy as creating a variable looking for the location of the backticks and making sure that the backticks aren't in invalid positions.


Fixing Snippet 2
---

When it comes to working with the nested ones, I think using something like an if statement to assign a new location to the open and bracket to look for the closing bracket. Once the code is notified that there are multiple openeing brackets it can look for the corresponding closing and possible link.


Fixing Snippet 3
---

In __my__ implementation of MarkdownParse.java, the code is seperated by line. This means that if the link goes onto another line that it will never be detected by the code and be dismissed as invalid. There would not be a < 10 line code change that could account for this.

