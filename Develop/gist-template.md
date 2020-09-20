# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

Anchors specify the position of the pattern in relation to a line of text. For example, "^" is placed at the beginning of a string and "$" is placed at the end. "/b" and "/B" are used to notate word and not word boundries respectively. A word boundry is when a character appears specifically at the beginning or end of a word. Therefore, a not word boundry is every time the character appears regardless of its position within a word.

### Quantifiers

Quantifiers indicate the preceding token must be matched a certain number of times, and will match as many characters as possible. For example, b\w{2,3} in the string "b be bee bean beans" will match with "bee bean bean" ommiting the "s" in "beans."

### OR Operator

The Alternation Operator (also referred to as the "OR Operator") acts very similarly to the OR boolean. It matches one of a choice of regular expressions; if you put the alternation operator between any two regex, the result matches the union of the strings that match both a and b. For example, the regex b(a|e|i)d on the string "bad bud bod bed bid" would return "bad bed bid."

### Character Classes

Character classes match a character from a specific set. Examples include, but are not limited to: character set [ABC], negated set [^ABC], 

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
