# Automation

## Regular Expression:

a sequence of characters used to check whether a pattern exists in a given text (string) or not .

## Regular Expressions in Python

regular expressions are supported by the re module.

**re Functions:**

- ``` findall() ```function returns a list containing all matches.
- ```search() ```function searches the string for a match, and returns a Match object if there is a match.
- ``` split()```function returns a list where the string has been split at each match.
- ``` sub()```function replaces the matches with the text of your choice.
- ``` match()```function returns a match object if the text matches the pattern.
- ``` group()```functionreturns the string matched by the re.


## Basic Patterns: Ordinary Characters

The ```match()``` function returns a match object if the text matches the pattern. Otherwise, it returns None. 

**ex:**
```


pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")

```
output:
```
Match!
```

## Wild Card Characters: Special Characters:

Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression.


- . - A period. Matches any single character except the newline character.
- ^ - A caret. Matches the start of the string.
- $ - Matches the end of string.
- \ - Backslash. 
- \w - Lowercase 'w'. Matches any single letter, digit, or underscore.
- \W - Uppercase 'W'. Matches any character not part of \w (lowercase w).

## Grouping in Regular Expressions 

The group feature of regular expression allows you to pick up parts of the matching text.Parts of a regular expression pattern bounded by parenthesis () are called groups.

**ex**
```
statement = 'Please contact us at: support@datacamp.com'
match = re.search(r'([\w\.-]+)@([\w\.-]+)', statement)
if statement:
  print("Email address:", match.group()) # The whole matched text
  print("Username:", match.group(1)) # The username (group 1)
  print("Host:", match.group(2)) # The host (group 2)
```

**Output**

```
Email address: support@datacamp.com
Username: support
Host: datacamp.com
```

