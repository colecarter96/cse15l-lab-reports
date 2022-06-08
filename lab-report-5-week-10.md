
Week 8 Lab Report
===

Written by Cole Carter
---

Finding the Differences in Outputs
---

* For this portion of finding the tests that make different ouputs I used the manual method of looking through a couple tests that look like they would perform differently with my implementation of MarkdownParse

The Links to the Tests
---

* The first link was test [14.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/14.md) and the second link was test[194.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.md)

Test 14
---

* When looking at VSCode Preview it shows that there should be no links in this markdown file

* For test one my implementation output this:
![Image](screenshots/Screen%20Shot%202022-06-08%20at%2011.54.13%20AM.png)
or `[]` and didn't catch any links. While the other implemenetation outputs this:
![Image](screenshots/Screen%20Shot%202022-06-08%20at%2011.46.36%20AM.png)

  and catches `/foo` as the link.

Test 194
---

* When looking at VSCode Preview it shows that there should be no links in this markdown file

* For test one my implementation output this:
![Image](screenshots/Screen%20Shot%202022-06-08%20at%2011.54.45%20AM.png)
or `[]` and didn't catch any links. While the other implemenetation outputs this:
![Image](screenshots/Screen%20Shot%202022-06-08%20at%2011.52.07%20AM.png)

and catches `url` as the link.


Sample To Debug 
---

* The repo that was given for file 9 catches all of the false links:
    ![Image](screenshots/Screen%20Shot%202022-06-08%20at%2012.14.54%20PM.png)
    This can be changed by looking to see if the tick marker is in front of the open or close brackets. This would be done in a similar way of finding the brackets and you can check if the index is before or after the bracket and then discount the following link as invalid.