# RegEx-Guide

Regular expressions (regexs) are objects that help with filtering and verifying strings. They are typically used to verify values such as email addresses, URLS, passwords, and more. In this guide, I will use an example regex that is commonly used to verify email addresses to provide an overview of how regexs are created and used in programming. 

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

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)