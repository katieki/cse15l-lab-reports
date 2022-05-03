# **Week 4 Lab Report 2**

---

## Bug #1:

The code had a bug that would compile an error when there would be any lines after the links.

[Bug #1 Error File](/Users/katiekim/Documents/GitHub/markdown-parser/test-file2_us.md)

![Image](./Screen%20Shot%202022-05-02%20at%209.14.35%20PM.png)

* This page shows the 3 links and the line printed after the links, that would cause the bug.

![Image](./Screen%20Shot%202022-04-24%20at%209.58.10%20PM.png)

* This is what would show up when running the bugged code, where it would throw an exception.

> We implemented two new lines to the code where we would break the code right away if there is no bracket for the link.

![Image](./Screen%20Shot%202022-04-22%20at%204.28.54%20PM.png)

* This is what shows up in the github repo after committing and pushing the changes we made in my remote computer. The changes we made in the code are displayed.

The bug was caused by the lack in main code that did not account for if there was anything that should break the while loop. The bug therefore caused a symptom to appear in the terminal in the form of an exception after running the code with the failure inducing input, which was the line after the links.

---

## Bug #2

The code had a bug that would throw an error when there would be any images added.

[Bug #2 Error File](/Users/katiekim/Documents/GitHub/markdown-parser/test-file3_us.md)

![Image](./Screen%20Shot%202022-05-02%20at%209.16.28%20PM.png)

* This page shows the 3 links and a line in between the links that creates an image, which is what causes the bug.

![Image](./Screen%20Shot%202022-04-24%20at%2010.11.55%20PM.png)

* This is what would show up when running the bugged code. It will throw an exception.

> We implemented three new lines to the code where if there is an exclamation point before the open bracket, it will pass that lne of code.

![Image](./Screen%20Shot%202022-04-24%20at%2010.10.55%20PM.png)

* This is what shows up in the github repo after committing and pushing the changes we made in my remote computer. The changes we made in the code are displayed.

The bug was caused by the lack in main code that did not account for if there is an image call, as the image call also involves brackets. The bug therefore caused a symptom to appear in the terminal after running the code with the failure inducing input, which was the image call.

---

## Bug #3:

The code had a bug that would compile an error when there would be incorrect syntax when making a link.

[Bug #3 Error File](/Users/katiekim/Documents/GitHub/markdown-parser/test-file4_us.md)

 ![Image](./Screen%20Shot%202022-05-02%20at%209.16.38%20PM.png)

* This page shows the 3 links and the line printed after the links, that could cause the bug.

![Image](./Screen%20Shot%202022-04-24%20at%209.58.10%20PM.png)

* This isn't the exact screenshot of the exception thrown but there is an exception thrown in a similar manner in the command line when running the code with the faulty input.

> We implemented new lines to the code where we would move on to the next line of code if the synax for the link calling line is missing a close parenthesis.

![Image](./Screen%20Shot%202022-04-24%20at%2010.20.22%20PM.png)

* This is what shows up in the github repo after committing and pushing the changes we made in my remote computer. The changes we made in the code are displayed.

The bug was caused by the lack in main code that did not account for when the syntax for the link calling line is missing a closed parenthesis. The bug therefore caused a symptom to appear in the terminal after running the code with the failure inducing input, which was that line without the closed parenthesis.

---