# Regex-Insight
Regex to Validate Javascript Form on a Website.

## Summary

In this tutorial I will explain to you the following regex expression and what are those special characters stands for or their tasks on implementing a javascript function.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
We want to use regex to validate a JavaScript form on a website to ensure only real email addresses are entered. An email address must have an @ symbol and at least a two-letter top-level domain like .co, org, or .com, as shown below.

^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$

An @ sign, the expression wants to match this character exactly so we put it specifically out the group of regex expression.

### Anchors

The most important anchors in this line is (Caret)^ and (Dollar sign)$.
Both anchors can be used together within a regular expression to match a specific group of characters on a single input line.
As both anchors are present, at the beginning and end of the line, our expression describes all characters.

### Quantifiers

The Curly bracket{2,} creates specific quantifier range. 
The curly bracet quantify the group to 2 or more matches.
The curly-bracet quantifier at the end signifies the email ending should be two or more characters in length, 

### OR Operator
The plus sign(+) outside the brackets indicates that one or more preceding grouped characters should be matched.

### Character Classes

The backlash \ characters indicates the character should be special.
A period \. is a special character in ERE, we must escape it (include a backslash), so we can match the period character exactly.


### Grouping and Capturing

Ranges can be added together in a single group with additional characters. For example, the regular expression [a-fA-F0-9] will match any single hexadecimal digit.
You can specify a group by adding a caret as the first character. Therefore, [^a-zA-Z] will match any non-letter character and [^0-9] will match any non-numeric character.

### Bracket Expressions
[a-zA-Z0-9._%+-] First group is indicating that user should use lowercase and uppercase letter characters, numbers, and the specific characters for a period, underscore, percent sign, plus sign, and minus sign for their email.

[a-zA-Z0-9.-] Second group indicates that user should include lowercase and uppercase letter characters, numbers, and the specific characters for a period and minus sign. Eliminating some of the special characters removes all of the legal non-Unicode domain name characters.

[a-zA-Z] Third group indicates that user should use lowercase and uppercase letter characters with a two-character requirement to eliminate non-Unicode top-level-domains.

### Look-ahead and Look-behind

As our goal is to exclude any characters that are not letters from the a to z range, we need to add assertions to the expression. 
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$ as we put the anchors ^ at the beginning and $ at the end which will match the beginning and end of the expression to
any combination of lowercase and uppercase letters and numbers, as well as periods, underscores, percent signs, plus signs, and minus signs.

## Author

The author is currently on UC Berkeley bootcamp. Link to the author Github at [ALMA-DEv914](https://github.com/ALMA-DEV914)
