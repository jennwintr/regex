# Regex

## Summary

Regex, also known as regular expressions, are patterns used to match character combinations in strings.  It is useful in extracting information from any text when it is included in a code or search algorithms. 
- Example: regex code to match an email address:
```
 /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/
```

Search pattern for regex has boundaries by 2 slash characters `/`.
- For example: 
```
/abc/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are asserted at a particular place in the search.  It allows the user to match strings that begin or end  with certain characters.
- `^` beginning of string
- `$` end of string
- Example:  
```
- ^The :match any string that starts with 'The'.
- End$  :match any string the ends with 'End'.
- ^The End$ :match exact string.
- hello  :match any string with the exact text 'hello' 
```

### Quantifiers
Specifies how many characters a string must present in the input for a match. Quantifiers are `* + ? and {}`.
- Example: 
```
- abc* :match a string that has 'ab' followed by zero or more 'c'.
- abc+  :match a string that has 'ab' followed by one more 'c'.
- abc?  :match a string that has 'ab' folllowed by zero or one 'c'.
- abc{2}   :match a string that has 'ab' followed by 2 'c'.
- a(bc)*   :match a string that has 'a' followed by zero or more copies of 'bc'.  
```

### Grouping and Capturing
- `()` :this operator is used to extract information from strings or data. Groups will be shown in an array. 
- `(?:)`  :using `?:` disables the capturing group
- `(?<>)`  :using `?<>` puts a name to the group

Example:
```
- a(bc)  :creates a capturing group with 'bc'
- a(?<food>bc)  :?<food> named the group 'food'
```

### Bracket Expressions

### Character Classes
 Character classes distinguishes different kinds of characters such as letters and numbers. 
```
- [] - one character:
   - Ex: [abc] means 'a' or 'b' or 'c'
- \d :matches one numerical character from [0-9]
- \w :matches one character from [a-z]
- \s :matches white space character
- \D :matches a single non-digit character
- \W :matches a single non-character that is 'a-z'
- \S :matches a single non-white space
```

### OR Operator
 OR operators are `| or []`.
- Example: 
```
a(b|c) :matches a string that has 'a' followed by 'b' or 'c'.
a[bc]  :matches a string that has 'a' but not capture 'b' or 'c'.
```

### Flags
A flag value is added at the end of the slash character 
- **g** : global, which does not return after the first match.  It restarts the after the end of the last search.
- **m** : multi-line, enable with ^ and $. This will match the start and end of a line.
- **i** : insensitive, which makes the whole expression case-insensitive

Example: 
```
- /Hi/g  :matches all the 'Hi'
- /Hi/m  :matches the beginning and ending of each line with 'Hi'
- /Hi/i  :matches all 'hi' regardless if the letters are upper or lowercase 
```

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
