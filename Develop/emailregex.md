# Email Regex - Tutorial

This tutorial will show you how to use the expression ```/([a-z0-9 .-]+)@([da-z.-]+).([a-z.]2,6)$``` to match emails using regex. This is useful when using applications/technologies like Node (Inqurier) or MongoDB to validate emails.

## Summary

A regular expression is a string of characters that describes a pattern to look for. This is widely used to find patterns in a string, find and replace characters in a string, and validate input. This tutorial will go through the different parts of a regex and how they relate to email matching.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
The anchors used in this regex expression for matching an email are, ```^``` which indicates the string's start, and ```$to```, which indicates the string's end. The regex will end at ```$``` because ```(m)```, or multiline, is not allowed.

### Quantifiers
The ```+``` operator, which connects the user's email name + email service + ```.com```, is one of the quantifiers in this regex. A second quantifier for this regex is ```2,6```, which allows a match range of 2-6 characters for the ```[a-z]``` character set.

### Character Classes
This expression's character class is ```d```, which corresponds to a single character that is a digit from 0 to 9. It can only fit single digits like "5", but not "99."

### Grouping and Capturing
Capturing group #1 in this expression is ```([a-z0-9_\.-]+)``` that matches the user email name. The second capturing group is ```([\da-z\.-]+)``` which will match the email service. Then lastly, capture group #3 is ```([a-z\.]{2,6})``` to capture the ```.com```.

### Bracket Expressions
The character sets ```[a-z0-9_.-]```, which matches every letter a-z and is case sensitive, are used for email validation. It also matches characters ```_```, ```-```, and ```.```; ```[da-z.-]```, which matches a single digit from 0-9, any character a-z (case sensitive), and the characters ```.``` and ```-```.; ```[a-z.]``` matches any character a-z(case sensitive) and the character ```.```.

### Greedy and Lazy Match
Greedy matches are included in this regex. It will match as many times as possible, giving back as required, since it contains the ```+``` Quantifier. When matching 2,6 for the last capture set, another greedy Quantifier ```{}``` is used in this regex.

## Author

Ashton Pierce - [Github](https://github.com/apierce17)
