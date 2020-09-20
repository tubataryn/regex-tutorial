# Regex Introduction

Searching a document for errors or specific instances can be very difficult, especially when there are over a few hundred lines of text to go through. Regular expressions can help by searching for specific instances or characters throughout the text while ignoring what is not being searched for.

## Summary

In this document, I have described a few of the fundamentals of regex and given examples of proper syntax. While some of the components are slightly more advanced, like lookarounds and backreferences, they are no less useful than their more straightforward counterparts like quantifiers, anchors, and character classes. Below is a table of contents for all the elements covered in this tutorial.

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

There are three primary components in a regular expression: anchors, character sets, and modifiers. Anchors specify the position of the pattern in relation to a line of text. Character sets match one or more characters in a single position. Modifiers dictate how many times the specified character set is repeated.

### Anchors

Anchors specify the position of the pattern in relation to a line of text. For example, "^" is placed at the beginning of a string and "$" is placed at the end. 

### Quantifiers

Quantifiers indicate the preceding token must be matched a certain number of times, and will match as many characters as possible. For example, b\w{2,3} in the string "b be bee bean beans" will match with "bee bean bean" ommiting the "s" in "beans."

### OR Operator

The Alternation Operator (also referred to as the "OR Operator") acts very similarly to the OR boolean. It matches one of a choice of regular expressions; if you put the alternation operator between any two regex, the result matches the union of the strings that match both a and b. For example, the regex b(a|e|i)d on the string "bad bud bod bed bid" would return "bad bed bid."

### Character Classes

Character classes match a character from a specific set. Examples include, but are not limited to: character set [ABC], negated set [^ABC], range [A-Z], dot (selects everything) ., match any [\s\S], word \w, not word \W, and many more.

### Flags

Expression flags change how the expression is interpreted and follow the closing forward slash of the expression such as "/.+/igm". Examples of flags include: ignore case "i", global search "g", multiline "m", unicode "u", sticky "y", and dotall "s".

### Grouping and Capturing

Groups allow you to combine a sequence of tokens to operate on them together. Capture groups can be refereced by a backreference and accessed separately in the results. Examples of groups include: capturing group (ABC), named capturing group (?<name>ABC), numeric reference "\1", and non-capturing group (?:ABC).

### Bracket Expressions

Bracket expressions are special kinds of character classes. A hyphen creates a range and a caret at the start negates the bracket expression (ex. [A-Z] or [^ACB]). The main syntax difference is that a backslash is not a metacharacter in a bracket expression. Therefore the expression []\d^-] matches the characters ], \, d, ^, and -.

### Greedy and Lazy Match

A greedy match, such as quantifiers, matches as many characters as possible. A lazy match causes the quantifier to match as few characters as possible. Quantifiers by default are greedy, but can be made lazy by adding "?" at the end of the expression. Using the example in quantifiers above, the same expression of b\w+? in the string "b be bee bean beans" will return "be be be be" ignoring the rest of the letters in the words of the string.

### Boundaries

A word boundry is when a character appears specifically at the beginning or end of a word. Therefore, a not word boundry is every time the character appears regardless of its position within a word. "/b" and "/B" are used to notate word and not word boundries respectively. 

### Back-references

Backreferences match the same text as previously matched by a capturing group. To find the number of a particular backreference, scan the regex from left to right and count the number of opening parentheses of all the numbered capturing groups. The first parenthesis starts backreference number one, the second number two, etc. For example, in the regex <([A-Z][A-Z0-9]*)\b[^>]>.*?</1> the tag </1> references ([A-Z][A-Z0-9]*).

### Look-ahead and Look-behind

Lookahead allows you to look after your main pattern withut including it in the result, similarly lookbehind allows you to look before the pattern. There are positive and negative lookarounds, positive specifies a gorup that can match before or after the pattern and negative specifies a group that cannot. For example, a positive lookahead would be (?=ABC) while a negative lookahead would be (?!ABC). Conversly, a positive lookbehind would be (?<=ABC) and a negative lookbehind would be notated as (?<!ABC).

## Author

Taryn is an aspiring full-stack web developer with a BA in Music from the University of Wisconsin Milwaukee. She has always been interested in technology as well as music and hopes to find a way to marry the two in her career. Her github can be viewed [here](https://github.com/tubataryn)!
