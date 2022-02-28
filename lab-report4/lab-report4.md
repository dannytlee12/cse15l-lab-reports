# Lab Report 4
## My repositories
[My Repository](https://github.com/dannytlee12/markdown-parse)

[Reviewed Repository](https://github.com/ajwboi/markdown-parse)


## Testing
![Image](SnippetTests.png)
* This is the code for the tests that I used for both my MarkdownParse and the one that I reviewed.
* For snippet1, the correct links are [`google.com, google.com, ucsd.edu]
* For snippet2, the correct links are [a.com, a.com(()), example.com]
* For snippet3, the correct links are [https://ucsd-cse15l-w22.github.io/]

## My Implementation
![Image](MySnippet1.png)
* Above is the output that I got for snippet1. A Failure.

![Image](MySnippet2.png)
* Above is the output that I got for snippet2. A Failure.

![Image](MySnippet3.png)
* Above is the output that I got for snippet3. A Failure.

## Their Implementation
* This section of the report is for the group that I reviewed.
![Image](TheirSnippet1.png)
* Above is the output that they got for snippet1. A Failure.

![Image](TheirSnippet2.png)
* Above is the output that they got for snippet2. A Failure.

![Image](TheirSnippet3.png)
* Above is the output that they got for snippet3. A Failure.


## Imporving my MarkdownParse

#### Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.
* I do think that there is a small code change that could be made to fix this error. I could validate backticks as a character, whenever they are found within a pair of brackets or parenthesis so that they are able to be a part of a link or a tag.




#### Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.
* I think that this will only require a small change in code. In the case of nested parenthesis or brackets, I can simply look for the most external pair. This will allow brackets or parenthesis to be inside the link or the tag for he link.



#### Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
* This may require a larger code change. I would have to look at the markdown file as a continuous string of chracters, instead of looking at each individual line. I would probably do this by creating another local variable that keeps track of the last finished link/image, allowing me to parse from that point onwards.
