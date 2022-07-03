# Regular Expressions (RegEx) Tutorial

For web developers, it is very important to be able to validate user inputs in various types of forms. One of those validation methods is the use of what is known as regular expressions (RegEx for short). For this tutorial, I will be explaining what a Regular Expression (RegEx) is all about, and how it is used to verify an email address. A regular expression (or RegEx) is a series of characters which define a specific search pattern. One of the things RegEx is used to look for is certain patterns of characters within a string, which can be very useful when it comes to validating emails using applications such as Node.js or MongoDB.

## Summary

In this tutorial, I will be covering and breaking down what constitutes a Regex component that is used to match email values.

Matching email:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
The first component I will be going over are anchors. They are located at the beginning at the end of the string, as shown in the snippet example below. While the /^ anchor signifies the beginning of a string or expression with the characters that follow it, the $/ anchor represents the end of it with the preceding characters. 


Code snippet example: `/^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$/`
### Quantifiers
The next component I would like to touch upon will be quantifiers. They set the limits of the string that matches the RegEx, and frequently include the minimum and maximum number of characters the regex is looking for. Because quantifiers are greedy, they will match as many characters as possible. Quantifiers are represented by the symbols, "* + {}". In the example below, the "+" denotes the value in the parentheses matches the pattern one or more times. While not listed in the example below, the " * " symbol matches the pattern zero or more times, and the "?" symbol matches the pattern zero or one time. The example below includes curly brackets "{}", which can provide three different ways to set limits for a match: in the example below, { 2, 6 } means that the string matches the pattern for a minimum of 2 times to a maximum of 6 times.

Code snippet example: /^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/
### Bracket Expressions
Bracket expressions for validating email addresses are patterns inside a set of square brackets which represent a range of characters we would like to match. Bracket expressions are also known as positive character groups because they outline the characters we would like to include in the RegEx. In the example listed below, the character sets of [a-z0-9_\.-] matches any letter from "a" through "z" and is case sensitive, and matches the characters 0 through 9 plus the characters "_" , "-" , and ".".

Code snippet example: /^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/
### Character Classes
Character classes define a set of characters by matching a character from a specific set. An example of a character class listed earlier in the tutorial is the bracket expression that includes positive and negative groups. Another example is depicted in the code snippet example below as "\d", which would match a single digit character between 0 and 9.

Code snippet example: /^([a-z0-9_\.-]+)@([`\d`a-z\.-]+)\.([a-z\.]{2,6})$/
### Grouping and Capturing
Grouping is used to break sections up in order to check multiple parts of a string to determine that different sections fulfill different requirements. This is done by the use of parentheses, as shown in the example below. In addition to grouping, capturing groups is used to capture the matched character sequences for possible re-use. In the example below, ([a-z0-9_\.-]+) is used to capture the username, then ([\da-z\.-]+) is used to capture the domain name, and ([a-z\.]{2,6}) would be used to capture the top-level domain (TLD).

Code snippet example: /^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/

### Greedy and Lazy Match
In this section, I will explain greedy and lazy matches. Indicated by the "+" quantifier, a greedy pattern is always looking for the longest possible string, and will always attempt to repeat a sub pattern many times as possible before backtracking to explore shorter matches. On the other hand, a lazy pattern is looking for the shortest possible string while attempting to repeat a subpattern as few times as possible. While absent from the code snippet example below, a quantifier can be made lazy by appending the "?" symbol to an existing quantifier.

Code snippet example: /^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]{2,6})$/
## Author

This tutorial has been created by Hiro Kagei.

Contact Me:
### [GitHub](https://github.com/hkagei)
### [Email](k_dawg_1022@hotmail.com)
