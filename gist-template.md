# JS Regex Tutorial

This file explains the components of the reqular expression (regex) for matching a hexadecimal value and describes in detail how each component works.  Regular expressions are a series of character that define a search pattern.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

We'll call the following regex example 'Matching a Hex Value':
* Matching a Hex Value: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Here is a brief summary of the above regex breaks down and we'll get into more detail later:

* The string must begin with the literel character #
* The string can contain any letter characters from a-f
* The string can contain any number characters from 0-9
* The string must contain a total of 6 or 3 characters after #

An example of a hex value is #3cb371 which is for a shade of the color green.

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
Grouping constructs indicate groups and ranges of expression characters. The grouping construct in our 'Matching a Hex Value' regex is ([a-f0-9]{6}|[a-f0-9]{3}). Inside the grouping construct is the OR Operator (|), the charater classes and the quantifiers. 

### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match. These patterns are known as bracket expressions.  In the 'Matching a Hex Value' regex, it is the [a-f0-9] component, where the value is made up of characters between a-f and/or 0-9.  The quantity of charachers will match the amount detailed in the proceeding quantifier {6} or {3}.

### Character Classes
Character classes distinguish kinds of characters such as, distinguishing between letters and digits. For our 'Matching a Hex Value' regex, the [a-f0-9] is the character class which is repeated twice with different quantifiers attached to each one.

Inside the character class there are two ranges mentioned, a-f and 0-9. As long as the characters used in the character classes are a-f and/or 0-9 and as long as the proceeding quantifier is matched, the value used as the hex value will work in the regular expression.

If the character class were [w-z], the characters that would match would be: 'w', 'x', 'y' or 'z'.

### The OR Operator
The OR Operator is the pike character (|).  In our expression, it is contained within the grouping construct between the two character classes and their quantifiers.  In our expression it means that we can have 6 OR 3 characters after the #.

### Flags

### Character Escapes

## Author

Joe is a full stack MERN developer focused on mobile-first design and development.  When he is not developing, he enjoys hiking, jogging, and reading up on the latest trends in web development.

GitHub:
https://github.com/jlewisit

Portfolio:
https://jlewisit.github.io/portfolio/