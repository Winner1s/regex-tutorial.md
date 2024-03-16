# Regex-Tutorial

A Regular expression tutorial to explain how a regular expression also known as regex can be used to identify character patterns for email functions by breaking down each part of the expression and describing what it does.

## Summary

Tutorial for email regular expression. A regex can be used for many things including matching the following items; hex value, email, URL, HTML tag, etc. This tutorial will specifically focus on how a regex can be used to match a email address. The following code is an example of what a regex can be used to verify that user input is a valid email address.

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

An anchor in a regex is used to identify the beginning and end of a string. The beginning anchor can be identified by the "^" symbol and the ending of a string can be identified by the "$" string.  For example, in the above example of what a regex looks like for an email address, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, notice the "^" symbol directly after the / and the "$" right before the final /. These symbols identify the complete regex collectively. Please see below for examples of quantifiers and their meanings;

### Quantifiers

Quantifiers indicate numbers of characters or expressions to match. In other words, quantifiers are metacharacters that specify how many times the previous character or group should be matched.

-"+" - + means the previous character must occur one or more times.
Ex. ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

        Notice there are two + symbols in the example regex.  They indicate that the previous character or array must occur at least 1 or more times. So this array - [a-z0-9_\.-] and this array,  [\da-z\.-], must occur at least once in one form or another.

-"?" - ? means that the preceding character is optional, so instead of occuring 1 or more times, this character can exist or not exist without creating an error for the email address regex or other regex being used.

-"_" - _ means that the preceding character matches zero or more times.

-"{}" - {} curly brackets are used to match a variable amount of occurences exactly.

-"{n,}" - {n,} curly brackets with a comma also matches a variable amount of occurrences, but it is not exact. It represents a variable number or more.

-"{n,m}" - {n,m} curly brackets with two different variables indicates a range of different occurences between the two variables.

### OR Operator

- the or operator is represented by the "|" symbol. This symbole indicates that an expression written as [abc] could also be written as (a|b|c).

### Character Classes

- "." a period represents any character except characters on a new line
- "\w" a backslash lower case w repesents words
- "\W" a backslash with an uppercase W indicates that there are no words
- "\d" a backslash lowercase d represents digits
- "\D" a backslash uppercase D indicates that an expression is not digits
- "\s" a backslash lower case s represents whitespace
- "\S" a backslash uppercase S indicates that an expression is not whitespace
- "[abc]" - indicates that an expression can be a,b, or c
- "[^abc]" when the "^" symbol is added to [^abc], this indicates that an expression is not a,b, or c
- "[a-z]" a-z indicates that the character id s range between a and z
  In the expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ a-z represents a range of characters between a and z and 0-9 represents a range of number characters between 0 and 9.

### Flags

Flags are optional arguments used to modify a expression pattern. a few of the most common flags in a regex are listed below:

g —Global search: the regex should be tested against all possible matches in a string.

i —Case-insensitive search: case should be ignored while attempting a match in a string

m —Multi-line search: a multi-line input string should be treated as multiple lines

In the example, there are no flags being used.

### Grouping and Capturing
Grouping is using symbols or parenthesis to separate different areas of a regex.  For example in our example regex, there are three different groups.  Each group is separated by parenthesis.

 /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

 - group 1 (user created email address)- ([a-z0-9_\.-]+)
 - group 2 (domain name or email service, (hotmail, outlook, gmail etc.))- ([\da-z\.-]+)
 - group 3 (domain extention(.com, .gov, .net etc.))- ([a-z\.]{2,6})


### Bracket Expressions
Brackets in a regex do not mean "array" they indicate that there is a range of characters that can be used as a specific part of the regex.  For example in the above example for grouping, notice that every group also includes brackets.  Each bracket is an explanation of characters and character types that can be included.  

- group 1 - ([a-z0-9_\.-]+) - everything inside of the bracketed area of group 1 in our example can be used as the regex for the user created email.  So the user created email can include letters a-z, numbers 0-9, and can also include an underscore or a hypen.  


### Greedy and Lazy Match
The "?" symbol can be used to make quantifiers lazy.  When a quantifier is lazy, it will match the minimum amount of quantifiers.  

When a quantifier is greedy, the search will back track until the pattern is complete.

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
