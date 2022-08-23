# Regex Tutorial

Regex, formally known as regular expression, is a string of letters that designates a text search pattern. Such patterns are typically utilized by string-searching algorithms for input validation or "find" or "find and replace" operations on strings.

## Summary

This article explains how to use Regex to find a Hex value within a body of text.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/ is the syntax I'll be employing.

Colors can be identified using hex codes. It always follows a six-digit alphanumeric pattern.

The regex string I'm using will only return lowercase letters a, b, c, d, e, or f or the numerals 0, 1, 2, 3, 4,5, 6, 7, 8, or 9 and a # Number Sign character.

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

The example string's beginning caret and ending $ dollar symbol both function as anchors. 
/^#? ([a-f0-9]{6}|[a-f0-9]{3}) $/

-The string to which the regex pattern is applied begins with a caret match

-A #Number Sign MUST appear at the beginning of the string, and it is a literal character after 
the commencing caret.

-The final character of the string to which the regex pattern is applied matches the dollar sign ($). This represents the string's conclusion.


### Quantifiers

The number of times the previous token will be matched is indicated by each quantifier. The example syntax uses three quantifiers. /^#? ([a-f0-9]{6}|[a-f0-9]{3}) $/

-the initial dollar sign ($) ( which I will also go over in the Greedy section) This means that 0–1 times will the # Number Sign match.

-{6} This indicates that there will be 6 characters in that set that match the preceding token [a-f0-9].

-{3} This indicates that there will be three characters in that set that match the preceding token [a-f0-9].


### OR Operator

The vertical line or pipe (|) OR operator is used in the example syntax. Between the two kinds of characters, there is a | Pipe. This produces two different groupings. As a result, either group can be found and matched by the search.

/^#? ([a-f0-9]{6}|[a-f0-9]{3}) $/

-The first option is located before the | pipe and returns 6 characters from [a-f0-9].

-Three characters will be returned by the second option following the | Pipe.


### Character Classes

Between square brackets [] are character classes. They're employed to compile a list of permitted characters. There are two different character classes in the sample syntax. The quantifier is what causes each class to return a varied number of characters even if they appear to be exactly the same because they are.

[a-f0-9] is used in the example.

-a, b, c, d, e, or f are all case-sensitive single characters that fall inside the range a to f.

-The range 0–9 corresponds to a single digit in the following cases: 0,1,2,3,4,5,6,7,8, or 9.


### Grouping and Capturing

A capture group is formed by anything discovered within (round brackets). Everything contained within of that is handled as a single entity. Using the syntax in the example, /#? ([a-f0-9]{6}|[a-f0-9]{3}) One capture group ($/) has two character sets that are separated by an OR operator.


## Author

My name's Odin Russell. I'm a student at the University of Minnesota's full stack coding bootcamp. 

Check out my [GitHub profile!](https://github.com/LymphCode)