# JS Regex Tutorial

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

* Matching a Hex Value: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`


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
I'll break down the preceding 'Matching a Hex Value' regex in order to explore regex components in general.  A regex is considered a literal, so the pattern must be wrapped in forward slashes (/).  JavaScript also allows the use of a RegExp constructor.  The constructor function's parameters are enclosed in quotation marks instead of slashes.  

### Anchors
The ^ and $ characters are both considered achors.  The ^ anchor signifies a string that begins with the characters that follow it.  The $ anchor signifies a string that ends with the characters that precede it.

So in our 'Matching a Hex Value' regex, the string must start and end with something that matches the pattern #?([a-f0-9]{6}|[a-f0-9]{3}).

### Quantifiers
Quantifiers set the limits of the string that your regex matches.  The quantifiers used in the 'Matching a Hex Value' regex are ?, {6} and {3}.

? matches the previous token between zero and one times, as many times as possible, giving back as needed.

{6} matches the previous token exactly 6 times.

{3} matches the previous token exactly 3 times.



### Grouping Constructs

### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match. These patterns are known as bracket expressions.  In the 'Matching a Hex Value' regex, it is the [a-f0-9] component, where the value is made up of characters between a-f and/or 0-9.  The quantity of charachers will match the amount detailed in the proceeding quantifier {6} or {3}.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

Joe is a full stack MERN developer focused on mobile-first design and development.  When he is not developing, he enjoys hiking, jogging, and reading up on the latest trends in web development.

GitHub:
https://github.com/jlewisit

Portfolio:
https://jlewisit.github.io/portfolio/