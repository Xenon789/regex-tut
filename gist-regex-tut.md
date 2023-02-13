# Regular Expressions Tutorial

Hello! Welcome to this Regular Expression Tutorial. I will be summarizing and showing you what a Regular Expression (Regex) is. Thank you for viewing this gist! If you would like please follow and connect with me on linkedin as well :).

## Summary

Regular Expression: patterns used to match character combinations in strings. via MDN: (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

Example - United States Zip Code

`const re = '/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/'`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)

## Regex Components

### Anchors

The anchor starts and ends a regular expression. Anchors belong to the family of regex tokens that don't match any characters, but that assert something about the string or the matching process. via(http://www.rexegg.com/regex-anchors.html)
In the example (United States Zip Code):

`/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

The anchors are `^` and `$`.

### Quantifiers

Quantifiers are characters within the expression that indicate number of characters/expressions to match. via MDN(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

`/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

In this example the Quantifier is identifiable with a `+` and `{` these brackets `}`. The Quantifier `{2, 6}` means that the string must be at least 2 characters and less than 6 characters. The `+` symbol means that the characters identified before @ and . have 1 or more characters.

### Grouping Constructs

Grouping Constructs group multiple patterns as a whole. 

### Bracket Expressions

A Bracket Expression is an expression enclosed in square brackets. `[(expression)]`

Brackets will indicate which set of characters to match. 

`/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

In the expression above include ALL CHARACTERS identified within the brackets. An Example would be `[a-z]` meaning it would include all characters from a all the way to z.

### Character Classes

Character classes help to identify different types of characters. 

### The OR Operator

The OR Operator allows you to check multiple patterns for the expression being identified. An example of this is with Hex codes. Hex codes can be identified in 2 ways. A random set of 6 characters after the # or a series of 3 characters.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

As described above this expression accepts:
`[a-f0-9]{6}` 6 random characters
`OR` / `|`
`[a-f0-9]{3}` 3 characters

### Flags

Regular expressions have optional flags that allow for functionality like global searching and case-insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression. via MDN(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions#advanced_searching_with_flags)

A Flag is identified with backslashes. This allows the expression the ability to have properties. 

PROPERTIES:
* d - Generate indices for substring matches.
* g - Global search.
* i - Case-insensitive search.
* m - Allows ^ and $ to match newline characters.
* s - Allows . to match newline characters.
* u - "Unicode"; treat a pattern as a sequence of Unicode code points.
* y - Perform a "sticky" search that matches starting at the current position in the target string.

Syntax:

`const re = /pattern/flags;` or `const re = new RegExp("pattern", "flags");`

## Author

This tutorial was created by Xenon Santillan.

Thank you for viewing this tutorial!
