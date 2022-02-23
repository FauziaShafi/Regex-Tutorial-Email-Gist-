# Regex Tutorial: Matching an Email

For web developers, validating user inputs in various types of forms is of crucial importance. Since that is the starting point of data being sent between the client and the server, you need to make sure that everything starts off on the right foot - lest you end up with robust validation on the server end, which is oftentimes a bigger hassle than doing it on the front-end.
Regular expressions are sequences of metacharacters, denoting a pattern. These patterns can be of various kinds: a mix of letters with digits, special characters and even different language characters. An abbreviation for regular expression is RegEx or RegExp.

## Summary

Validating email is a very important point while validating an HTML form. In this page we have discussed how to validate an email using JavaScript :

An email is a string (a subset of ASCII characters) separated into two parts by @ symbol. a "personalInfo" and a domain, that is personalInfo@domain. The length of the personalInfo part may be up to 64 characters long and domain name may be up to 253 characters.

The personalInfo part contains the following ASCII characters.

Uppercase (A-Z) and lowercase (a-z) English letters.
Digits (0-9).
Characters ! # $ % & ' * + - / = ? ^ _ ` { | } ~
Character . ( period, dot or fullstop) provided that it is not the first or last character and it will not come one after the other.
The domain name [for example com, org, net, in, us, info] part contains letters, digits, hyphens, and dots.

Example of valid email id:  mysite@ourearth.com
Example of invalid email id: mysite.ourearth.com [@ is not present]

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

A regex is considered a literal, so the pattern must be wrapped in slash characters (/). If we examine the “Matching a email” regex, you'll see that this is true: 
Email format: The regular expression for email is


 <code>/^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/</code>

 To understand the regular expression we will divide it into smaller components:
 
 /^[a-zA-Z0-9._-]+:  Means that the email address must begin with alpha-numeric characters (both lowercase and uppercase characters are allowed). It may have periods,underscores and hyphens. 

 @:   There must be a ‘@’ symbol after initial characters.

[a-zA-Z0-9.-]+: After the ‘@’ sign there must be some alpha-numeric characters. It can also contain period (‘.’) and and hyphens(‘-‘).

\.: After the second group of characters there must be a period (‘.’). This is to separate domain and subdomain names.

[a-zA-Z]{2,6}$/: Finally, the email address must end with two to four alphabets. Having a-z and A-Z means that both lowercase and uppercase letters are allowed.
{2,6} indicates the minimum and maximum number of characters. This will allow domain names with 2, 3 and 4 characters e.g.; us, tx, org, com, net, wxyz.

### Anchors

The characters ^ and $ are both considered to be anchors. Anchors have special meaning in regular expressions.t They match a position before or after characters:

 ^ – The caret anchor matches the beginning of the text.
 $ – The dollar anchor matches the end of the text.

 <code>let str = 'JavaScript';
       console.log(/^J/.test(str));
</code>
 The /^J/ match any text that starts with the letter J. It returns true.

### Quantifiers
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for. There are two quantifiers within this regex, the first being + which is a greedy quantifier. This quantifier will allow connection for the users email+ email service + .com. The other quantifier is the {2,6}, this will match everything after the . 2-6 times to ensure it has at least 2 characters and no more than 6.

### Grouping Constructs
Each grouping construct is capturing pieces of data. 

### Bracket Expressions
Bracketed expressions within the email validation are within the []. Anything inside a set of square brackets ([]) represents a range of characters that we want to match. 


## Author
Check my work here - <a href="https://github.com/FauziaShafi">Github</a>
