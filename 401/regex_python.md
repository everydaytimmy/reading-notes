### Regex

https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial

In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:
```
import re
```

The `match()` function returns a match object if the text matches the pattern. Otherwise, it returns None. 

`.` - A period. Matches any single character except the newline character.
```
re.search(r'Co.k.e', 'Cookie').group()
'Cookie'
```
`^` - A caret. Matches the start of the string.

This is helpful if you want to make sure a document/sentence starts with certain characters.
```
re.search(r'^Eat', "Eat cake!").group()
```

`$` - Matches the end of string.

This is helpful if you want to make sure a document/sentence ends with certain characters.
```
re.search(r'cake$', "Cake! Let's eat cake").group()
```

`[abc]` - Matches a or b or c.
`[a-zA-Z0-9]` - Matches any letter from (a to z) or (A to Z) or (0 to 9).

 Character(s)	What it does
- `.`	A period. Matches any single character except the newline character.
- `^`	A caret. Matches a pattern at the start of the string.
- `\A`	Uppercase A. Matches only at the start of the string.
- `$`	Dollar sign. Matches the end of the string.
- `\Z`	Uppercase Z. Matches only at the end of the string.
- `[ ]`	Matches the set of characters you specify within it.
- `\`	∙ If the character following the backslash is a recognized escape character, then the special meaning of the term is taken.
        Else the backslash () is treated like any other character and passed through.
        It can be used in front of all the metacharacters to remove their special meaning.
- `\w`	Lowercase w. Matches any single letter, digit, or underscore.
- `\W`	Uppercase W. Matches any character not part of \w (lowercase w).
- `\s`	Lowercase s. Matches a single whitespace character like: space, newline, tab, return.
- `\S`	Uppercase S. Matches any character not part of \s (lowercase s).
- `\d`	Lowercase d. Matches decimal digit 0-9.
- `\D`	Uppercase D. Matches any character that is not a decimal digit.
- `\t`	Lowercase t. Matches tab.
- `\n`	Lowercase n. Matches newline.
- `\r`	Lowercase r. Matches return.
- `\b`	Lowercase b. Matches only the beginning or end of the word.
- `+`	Checks if the preceding character appears one or more times.
- `*`	Checks if the preceding character appears zero or more times.
- `?`	∙ Checks if the preceding character appears exactly zero or one time.
- `∙ Specifies a non-greedy version of +, *
- `{ }`	Checks for an explicit number of times.
- `( )`	Creates a group when performing matches.
- `< >`	Creates a named group when performing matches.

### shutil

The shutil module offers a number of high-level operations on files and collections of files. In particular, functions are provided which support file copying and removal. For operations on individual files, see also the os module.
