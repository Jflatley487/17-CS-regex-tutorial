# Matching an Email using Regular Expressions

In this tutorial, we will explore the regular expression used to match an email address. Regular expressions are tools for pattern matching in strings. They allow you to define specific search patterns and validate input. Understanding how regex works and how to break down each component of an expression is essential for web development.

The focus of this tutorial is on matching an email address: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This expression is comprised of dfifferent components that can be broken down to explain their functionality. Lets go! 

## Summary

The regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` is used to match an email address. It validates wheter a string represents a valid email address. 

Following is a list describing each component of this regex for better understanding.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors are special characters that assert a position within the string being matched. 
In our regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we have two anchors:

- `^`(caret) asserts the start of a string. It ensures that the email address starts with the specified pattern.
- `$`(dollar sign) asserts the end of the string. It ensures tha the email address ends with the specified pattern.

Together, these anchors ensure that the entire string is matched from start to end, allowing for a complete email address match.

### Quantifiers

Quantifiers define the number of times a character or group can occur. In the email validation regex, we use the following quantifiers:

- `+`(plus sign): Matches one or more occurences of the preceding element. It allows the local and domain parts of the email address to have one or more valid characters.
- `{2,6}` Matches the preceding elemnt between 2 and 6 times (both inclusive). It specifies the length range of the top-level domain (TLD) part of the email address.

These quantifiers ensure that the username and domain parts of the email address have the required number of characters.

### Grouping Constructs

Grouping constructs allow us to treat multiple characters as a single unit. In the email validation regex, we use grouping constructs to separate the local part, domain, and TLD of the email address.

For example, `([\da-z\.-]+)` matches and captures one or more digits, lowercase letters, dots, or hyphens in the domain part of the email address.

### Bracket Expressions

Bracket expressions define sets of characters that can match at a particular position in the pattern. In the email validation regex, we use bracket expressions to specify valid characters in the local part, domain, and TLD of the email address.

For example, `[a-z0-9_\.-]` matches any lowercase letter, number, underscore, dot, or hyphen in the local part of the email address.

### Character Classes

Character classes are used to match specific groups of characters. In the email validation regex, we use character classes to define valid characters for the local part, domain, and TLD of the email address.

For example, `[a-z0-9_\.-]` matches any lowercase letter, number, underscore, dot, or hyphen in the local part of the email address. Similarly, `[\da-z\.-]` matches any digit, lowercase letter, dot, or hyphen in the domain part of the email address. Lastly, `[a-z\.]` matches any lowercase letter or dot in the top-level domain (TLD) part of the email address.

These character classes ensure that only valid characters are accepted for each specific part of the email address, contributing to the overall validation of the email.

By understanding and combining these regex components – anchors, quantifiers, grouping constructs, bracket expressions, and character classes – you can create powerful patterns for validating email addresses.

### The OR Operator

The OR operator (|) allows us to match one pattern or another. In the email validation regex, we do not use the OR operator.

### Flags

Flags modify the behavior of a regex pattern. In the email validation regex, we do not use any flags.

### Character Escapes

Character escapes allow us to match special characters as literal characters. In the email validation regex, we do not use character escapes.

## Author

Hi, I'm Joey Flatley, a student at the UT Full Stack Web Development Bootcamp. When I'm not immersed in coding, you can find me pursuing my passion for rock climbing. I enjoy the challenge of solving problems and building innovative solutions. If you'd like to explore more of my projects, please visit my GitHub profile: Jflatley487. 
