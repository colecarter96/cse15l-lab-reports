Week 4 Lab Report
===

Three Code Changes to *Read Files* Better
---
      
Written by Cole Carter

1
---

**The Change Made to The Program**

![Image](screenshots/Screen%20Shot%202022-04-24%20at%2010.20.56%20PM.png)

**The Link and Failure Producing Output**


This change was in efforts to combat the problem in this [file](https://github.com/akluu/markdown-parser/blob/main/newTest.md).
When it runs it returns:

```[https://test.com, www.fakelink.com, www.facebook.com]```

 Which is the wrong output, the symptom is that it catches a fake link. It should be this:

 ``` [https://test.com, www.facebook.com]```

**The Bug and Symptom Relationship**

The relationship between the bug and the failure inducing output is that there is a line break where there are open and closed brackets on one line and then the next line has open and closed brackets with a fake link. To combat this, the file was broken to be read line by line instead of as one large string. In this case, 

2 
---

**The Change Made to The Program**

![Image](screenshots/Screen%20Shot%202022-04-24%20at%2010.27.38%20PM.png)

**The Link and Failure Producing Output**

The symptom producing test [file](https://github.com/akluu/markdown-parser/blob/main/newTest2.md) was now to have a open and closed bracket on the same line as the fake link, but with no test inside the bracket and a break inbetween the brackets and the open parenthesis. The failure inducing output was this:

```[https://test.com, www.fakelink.com, www.facebook.com]```

When it should've look like this:

```[https://test.com, www.facebook.com]```

**The Bug and Symptom Relationship**

Before the change the failure producing output was,

```[https://test.com, www.fakelink.com, www.facebook.com]```

 The bug in this case was that, before, the program wasn't checking to see if the link had to be set up the way that markdown wants it to be. The symptom for this bug was that it produced the wrong output and fell for the fake link.

3
---

**The Change Made to The Program**

![Image](screenshots/Screen%20Shot%202022-04-24%20at%2010.33.26%20PM.png)

**The Link and Failure Producing Output**

The failure producing [file](https://github.com/akluu/markdown-parser/blob/main/newTest3.md) for this had an image which is very similar to the way that links are written in markdown. The failed output looked like this

```[https://test.com, www.facebook.com, fakeImage.png]```

when it should've looked like this

```[https://test.com, www.facebook.com]```

**The Bug and Symptom Relationship**

The Bug in this situation is that the program cannot decifer the difference between an image and a link. The symptom is that, due to the bug, it prints out the incorrect links and takes in the png.


