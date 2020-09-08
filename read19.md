# Regular Expressions
Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. 

They are used at the server side to validate the format of email addresses or passwords during registration, 

used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.



![](https://www.optimizesmart.com/wp-content/uploads/2010/06/regex-cheatsheet-for-Google-Analytics1.jpg)

 useful functions provided by the re library, such as: compile(), search(), findall(), sub() for search and replace, split().


```
import re
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
#Match!
```

```
pattern = "cookie"
sequence = "Cake and cookie"

heading  = r'<h1>TITLE</h1>'
re.match(r'<.*>', heading).group()
#'<h1>TITLE</h1>'
```

```
heading  = r'<h1>TITLE</h1>'
re.match(r'<.*?>', heading).group()
'<h1>'
```
