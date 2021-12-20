# Regex Tutorial

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input

## Summary

Matching and Validating email addresess is an important part of creating forms and databases in websites. The ability to make sure a user is entering a valid and used email in an email server will make sure you have a clean database that can be used and to make sure that users are being validated.

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
There are multiple components of regex. A sequence of characters that defined the search pattern. To verify whether a given input string is a valid e-mail id match it with the following is the regular expression to match an e-mail id:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

### Anchors
There are two anchors used the the email validation regex:
- `^` - This is the begining of a string
- `$` - This is the end of a string

### Quantifiers
There are multiple quantifiers being used in this regex. The first example is the `+` used at the end of the first grouping construct. This quantifier means that the result has to have 1 or more of the potential elements outlined in that grouping construct. The `+` quantifier is used in the second grouping construct as well. Both of them are looking for a character that meets at least one of the criteria. Finally in the third grouping contstruct the `{2,6}` quantifier is used to signify that this grouping construct requires a character length between 2 and 6.

### Grouping Constructs
There are three separate grouping constructs in this regex example. 
The first one is `([a-z0-9_\.-]+)`
This grouping is looking for 1 or more characters that are a letter, number, and could include a `_`, a `-` or a `.`
The `\.` part is used to break up the special characters so that it doesn't also look for a term that includes `_.-` as one string. The regex is looking for any emails that contain either a period, underscore or hyphen in the start of the email address.

The next grouping construct is: `([\da-z\.-]+)`
This one is looking for any number and/or any letter or a `.` or a `-`. At least one character is required that meets the criteria. This the part of the email after the @ symbol.

The final grouping construct is: `([a-z\.]{2,6})`
This represents the part of the email address after the `.` used for the email domain (.com). 

The grouping is looking for anywhere between 2 or 6 characters that could be either a letter or a `.`
This means that the domain part of an email address can't include a number and has to have at least 2 letters and a max of 6.

### Bracket Expressions
A matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.
The bracket expressions are as follows:

`[a-z0-9_\.-]` This first expression is looking for any letter or number or a period, hyphen or underscore.
`[\da-z\.-]` This one is looking for any number or letter a period or a hyphen.
`[a-z\.]` Finally this one is looking for any letter or a period.

### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match.

Here are some of the other common character classes:

`.` -Matches any character except the newline character `(\n)`

`\d` -Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

`\w` -Matches any alphanumeric character from the basic Latin alphabet, including the underscore (). This class is equivalent to the bracket expression `[A-Za-z0-9]`.

`\s`-Matches a single whitespace character, including tabs and line breaks

Each of the last three character classes can be changed to perform an inverse match by capitalizing the letter character. For example, \D matches a non-digit character.


### Character Escapes
The escaped character in this regex example is the period denoted by \. in the class groupings. This is used to break up the special characters in the bracket expression so that the regex knows to return any results that also contain a period.

The Charachter Espace in this tutorial is `\.` in the clas group. This is so regex knoows to return any results contained in the period by breaking up the special charactes in the bracket expression.

## Author

Created by: <a href="">Christopher Petrevski</a>
