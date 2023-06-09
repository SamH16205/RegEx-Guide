# RegEx-Guide

Regular expressions (regexs) are a method used in programming to identify certain patterns within text. In JavaScript, they are objects that help with filtering and verifying strings. They are typically used to verify values such as email addresses, URLS, passwords, and more. In this guide, I will use an example regex that is commonly used to verify email addresses to provide an overview of how regexs are created and used in programming. 

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The above regular expression is used to verify email addresses. It does this by ensuring that a value follows the same structure and syntax that email addresses typically follow. When applied to a string, it checks to see if the string consists of a series of numbers, characters, or a combination of each followed by an "@" symbol, followed by a series of letters, followed by a ".", which is followed by another series of letters with a length between 2 and 6.

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

Anchors are represented by the symbols '^' and '$' and are used to define what a pattern begin or end with. Characters that come after the '^' symbol define the begginning of the target pattern, while characters that come before the '$' symbol define the end of the target pattern. In our example, ^([a-z0-9_\.-]+) this expressions means that the begining of the pattern can contain numbers, lowercase letters, underscores, slashes, periods or hyphens.
The end of the expressions, ([a-z\.]{2,6})$, specifies that end end of our pattern must contain lowercase letters only, and be between 2 and 6 characters long.


### Quantifiers

Quantifiers are regex symbols that specify how many times something must match the pattern in order to pass. They are as follows:
*- match the pattern zero or more times
+- match the pattern one or more times
?- match the pattern zero or one time
{n}- match the pattern n times
{n, }- match the pattern at least n times
{n,x}- match the pattern between n and x times

In our example above, the only quantifiers used are {2, 6}, which indicates that there must be between 2 and six consecutive lowercase letters, and +, which specifies that each pattern only needs to occur one time to be considered valid. In other words, it is not neccessary for the pattern to contain two or more consecutive characters of the same type. 

### OR Operator

The '|' symbol is used for "or" statements. For example, if we wanted to specify a pattern that begins with either an 'a', 'b', or 'c', we would write ^[a|b|c]. The example of the email regex above does not utilize the or operator. 

### Character Classes

Character classes are used to define a set of characters. The most used ones include:
. - match any character
\d - match any digit 0-9
\w - match any uppercase letter, lowercase letter, or digit 0-9.
\s - match any single whitespace character

The email regex example above uses '\d' to indicate that any number may be included in the pattern

### Flags

Flags are additional search parameters that are placed at the end of a regex. Some common ones include:
g- global: test against all possible matches
i- case-insensitive: ignore case during search. Regexs are case-sensitive by default
m- multi-line: treat multi-line strings as multiple lines

The example email regex does not use any flags

### Grouping and Capturing

Grouping involves separating portions of the regex into different groups with different search parameters and an optional connector. Patterns within brackets are groups. 

In the email regex, there are three groups: 
([a-z0-9_\.-]+): group one= any number, letter, underscore, period, hyphen or slash
@([\da-z\.-]+)\: group two= must be separated from group one with a '@' symbol only and contain only lowercase letters, digits, slashes, periods or hyphens.
.([a-z\.]{2,6}): group three= must be separated from group 3 with only a period and contain only lowercase letters and be between 2 and 6 characters.

Capturing refers to 

### Bracket Expressions

Brackets "[]" are used to specify character ranges we wish to match. [a-r] would return a match if a sequence of characters contains a lowercase letter between a and r. Similarly, [acrp], would return a match if a sequence of characters contains an a,c,r or p

### Greedy and Lazy Match

By default, regexs are greedy, meaning they will search for the longest possible match. To make a regex lazy, you can add a question mark to the end of the regex A completely lazy regular expression will stop searching after finding the shortest possible match. 

For example:
If we use the regex \a*\ to search the string "aaaaaaa", it will return the entire string. However, if we use the regex \a*?\ on the string, it will return a single 'a'. 

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)