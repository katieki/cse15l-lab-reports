# **Week 10 Lab Report 5**

---

## Different Outputs

I received different outputs for the tests given in the repository shared in Lab 9 using [my MarkdownParse](https://github.com/katieki/markdown-parser/blob/main/MarkdownParse.java) and the [MarkdownParse in the shared repository](https://github.com/nidhidhamnani/markdown-parser/blob/main/MarkdownParse.java).

> To find the tests with different results, I picked a few tests out manually that I thought would cause different bugs and made new tests in MarkdownParseTest. I ran these tests using `make test`.

---

## First Test

Here is the link to the first test file that produced different outputs:

[First Test-File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/489.md)

To find out what the output this test should produce, I used the [CommonMark Demo Site](https://spec.commonmark.org/dingus/).

![Image](./Screen%20Shot%202022-06-10%20at%209.39.28%20PM.png)

* Looking at this, I thought the output should be `[]` because there is a line break breaking the syntax.

I made the tests manually in the MarkdownParse testing file.

![Image](./Screen%20Shot%202022-06-10%20at%209.52.16%20PM.png)

In terms of my MarkdownParse implementation, the terminal produced an error:

![Image](./Screen%20Shot%202022-06-10%20at%2010.09.59%20PM.png)

While the shared implementation passed the test.

![Image](./Screen%20Shot%202022-06-10%20at%209.55.17%20PM.png)

This is a part of my MarkdownParse implementation:

![Image](./Screen%20Shot%202022-06-10%20at%2010.20.59%20PM.png)

> My MarkdownParse implementation had a bug that continued the loop to search for the close parenthesis when it should look for line breaks that breaks the syntax of the link. Maybe in the while loop that starts at line 12 should contain an `if` statement that breaks the loop if there is no close parenthesis by the end of the line.

---

## Second Test

Here is the link to the second test file that produced different outputs:

[Second Test-File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/530.md)

To find out what the output this test should produce, I used the [CommonMark Demo Site](https://spec.commonmark.org/dingus/).

![Image](./Screen%20Shot%202022-06-10%20at%2010.01.43%20PM.png)

* Looking at this, I thought the output should be `[]` as well, because the first attempted link is to create an image while the second does not have parentheses.

I made the tests manually in the MarkdownParse testing file.

![Image](./Screen%20Shot%202022-06-10%20at%2010.51.51%20PM.png)

In terms of my MarkdownParse implementation, the terminal produced an error:

![Image](./Screen%20Shot%202022-06-10%20at%2010.08.46%20PM.png)

While the shared implementation passed the test.

![Image](./Screen%20Shot%202022-06-10%20at%2010.06.32%20PM.png)

This is a method that is a part of the shared MarkdownParse implementation:

![Image](./Screen%20Shot%202022-06-10%20at%2010.53.29%20PM.png)

> The shared MarkdownParse implementation had a bug that did not look out for if there is a `!` before the open bracket. Maybe in the while loop that starts at line 56, make an `if` statement that breaks the loop if the index before the open bracket is a `!`.