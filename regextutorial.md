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
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

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

### OR Operator
 OR operators are `| or []`.
- Example: 
```
a(b|c) :matches a string that has 'a' followed by 'b' or 'c'.
a[bc]  :matches a string that has 'a' but not capture 'b' or 'c'.
```

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
`[]`, means exactly one character.
Example:  
```
[abc] means 'a' or 'b' or 'c'.
```

### Greedy and Lazy Match
Quantifiers,` * + {}`, are greedy operators.  They will match as much as possible.
Example:
```
"This is a <div>simple div</div> test."
   - <.+> will show a match of <div>simple div</div>
```

To make a Lazy match, you can add a ?  operator.  
```
Using the above example, a search with <.+?> will return just the div tag, <div> and </div>
```

### Boundaries
Boundaries are the places between characters, like a wall between adjacent characters.
- `\b`  :matches positions where one side is a word character and the other side is not a word character.
- `\B`,  matches all positions where `\b` doesn't match.


### Back-references
- `\1`, matches the same text that was matched by the first capturing group.
- `\2`, matches the same text that was matched by the second capturing group.
- The same goes for `\3`, `\4` and etc.

### Look-ahead and Look-behind
**(?=)**
Example: 
```
d(?=r), matches a 'd' only if is followed by 'r', but 'r' will not be part of the overall match
```

**(?<=)**
Example: 
```
(?<=r)d, matches a 'd' only if it comes before 'r', but 'r' will not be part of the overall match.
```

## Author

Jennifer Winter
https://github.com/jennwintr/
