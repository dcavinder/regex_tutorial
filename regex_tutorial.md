# Matching a Hex Value

A Regex or regular expressions are sequences of characters that define a search pattern for text. Regex are used to find specific information in code so that the user can manipulate, verify, and extract and do other tasks that relate to the targeted inofrmation. These tools are useful in finding and verifying user input such as e-mail addresses and phone numbers as well as finding other information that meets the perameters chosen.

## Summary

Below is an example of the regex used to match HEX values. As a UI/UX developer it is essential to be able to find color values and modify them efficiently.There are also many other reasons we may want to search for hex values. We can use a regex to aid our search and make those modifications. This document will breakdown the following regex into anchors, quantifiers, the OR operator, character classes, grouping and capturing, bracket expressions, and explain the difference between a greedy and a lazy match.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

Anchor: ^
example: `/^#`

Anchors give some information about the string. The ^ is an anchor that shows the beginning of the string must start with #. In the case of HEX values they always start with # which indicates a hexadecimal number as oppsoed to a decimal.

Anchor: $
example: `$/`

The $ anchor shows the pattern fully matches what the string should end with. 


### Quantifiers

Quantifier: ?
example: `/^#?`

In the above code snppet the question mark indicates a boolean which mean the next charcter is optional. In this case the # symbol is optional.
 
Quanitfier: {}
examples:`[a-f0-9]{6}`
         `[a-f0-9]{3}`

The {} quantifier shows how many time times the pattern before matches. In the code snippet above the `{6}` is is searching for 6 consecutive characters that meet the `[a-f0-9]` description (which I will address below).

### OR Operator

OR operator : |
example: `[a-f0-9]{6}|[a-f0-9]{3}`

the OR operator looks like a vertical pole in between 2 segments of code serving as a boolean statement. `4|5` is the same as saying 4 or 5. The snippet above is looking for 6 consecutive characters that meet this description `[a-f0-9]` or 3 consecutive charcters that meet this description `[a-f0-9]`.

### Character Classes

example: `[a-f0-9]`

Character classes give a range of characters from a specific set. for example in the code snippet above a-f is indicating the letters in the alphabet between and including a and f. The hyphen is used as short hand for all of the characters in between.

### Grouping and Capturing

Grouping and Capturing: ()
example: `([a-f0-9]{6}|[a-f0-9]{3})`

The () symbols group the regex inside. SO the `[a-f0-9]{6}` and `[a-f0-9]{3}` become one expression with the OR operator in the center.

### Bracket Expressions

Bracket Expressions: []
example: `[a-f0-9]`

Bracket expressions indicate a specific pattern of characters which are difined inside the brackets.

### Greedy and Lazy Match

example: `[a-f0-9]{6}`

A greedy match means the regex is going to find the longest possible string while a lazy match is looking for the shortest possible string. Adding the ? to make the # option in `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` allows for more matches making the match a greedy match.

## Author

Danielle Cavinder is a Junior Web Developer and Software Engineer. She has a passion for UX/UI developement and hopes to use a combination of her design background and smart coding to create beautiful and user friendly applications in the future.

GitHub: https://github.com/dcavinder
