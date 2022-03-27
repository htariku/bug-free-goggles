# Regex Tutorial Challenge: Matching an Email

In this Gist we will be explaining the use of a regular expression used to match an email. This is extremely useful when validating emails in node or MongoDB. 

## Summary

Regular expressions are patterns used to match character combinations in a string. You construct regex in two ways...Either by using a regular expression literal or by calling the constructor function of the Regex object. In this Gist we will be mainly going over the components of a regular expression that involves matching an email - /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
The anchors used to match an email are ^ which symbolizes the beginning of a string; as well as $ that symbolizes its opposite, the end of a string. 
### Quantifiers
The first Quantifiers in this regular expression we will go over is the +, which is basically connecting the email name to the email service and the email service to the .com (email name + email service + .com). The other quantifier is {2,6} which has set its range of numbers so that the minimum number is 2 and the maximum number is 6. In this instance for the character set [a-z\.], we will only be matched with a range of characters 2-6.
### Character Classes
In this regex, we are using the \d character class to match a single character or single digit number from 0-9.
### Grouping and Capturing
Group #1 = email name ([a-z0-9_\.-]+)
group #2 = email service ([\da-z\.-]+)
group #3 = .com ([a-z\.]{2,6})

### Bracket Expressions
In this regex we have three bracket expressions:
[a-z0-9_\.-]: this bracket is matching any lowercase letter from a-z and any character from 0-9. the ".", "-", and "_" matching literal dashes, periods, and underscores. 

[\da-z\.-]: This bracket is matching a single digit from 0-9 and any lowercase letter from a-z, as well as the characters "." and "-".

[a-z\.]: This bracket is matching characters that are lowercase a-z, followed by a period "." 

### Greedy and Lazy Match
This regular expression includes greedy matches because we use the + quantifier that matches 1 or more times. As well as the {} quantifier used to find a range of number 2-6 ({2,6}) for the purpose of our regex.
### Boundaries
\b is anchor, like that of $ and ^, where one side is a word character and the other side is not. There were no boundaries used in this regex to match an email 
### Back-references
Back references look for previous matched groups to look for an identical text. We did not use back references for our email regex 
### Look-ahead and Look-behind
look-ahead asserts what follows the current position in the string and look-behind asserts what is preceding the current position in the string. look-ahead and look-behind are not used to match an email. 
## Author

Aspiring software developer, learn more about my projects at my github page: https://github.com/htariku

