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

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
