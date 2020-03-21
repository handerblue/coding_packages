
Sample:
```
text = open("file", "r")

pattern = re.compile($RULE)
matches = pattern.finditer(text)

for match in matches:
  ...
  
```

```


\b  Word boundary
\B  Not \b

\d  Digit:0-9
\D  not \d

\w  word character: a-z, A-Z, 0-9, _
\W  not \W

\s  Whitespace, tab, newline
\S  not \s

.   Any Character Except New Line
^   Beginning of a String
$   End of a String

[]    Matches Characters in brackets
[^ ]  Matches Characters NOT in brackets
|     Either Or
( )   Group

Quantifiers:
*     0 or More
+     1 or More
?     0 or One
{3}   Repeat with exact number
{3,4} Repeat with range of numbers (Minimum, Maximum)


#### Sample Regexs ####

[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+


```

We can extract key words in one single match by using "()" and .group(). 
```
pattern = re.compiler(r"($group1)($group2)($group3)")
matches = pattern.finditer(text)
for match in matches:
  print(match.group(0))
  print(match.group(1))
  print(match.group(2))
  print(match.group(3))

```

ref: 
- https://github.com/CoreyMSchafer/code_snippets/blob/master/Python-Regular-Expressions/snippets.txt
- https://www.programiz.com/python-programming/regex
