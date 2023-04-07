# Regex Tutorial 

## Summary
***
This code can be used to match emails that follow a standard format. It uses regex components such as “@” and “.” to identify the necessary parts of an email address. It also looks for things like a username and domain name in the address. This code can be used to validate an email address to make sure it follows the correct format. This can help prevent users from entering incorrect information into forms.

Matching Email:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents
***
[Anchor] br
[Quantifiers] br
[OR Operator] br
[Character Classes]
[Flags]
[Grouping and Capturing]
[Bracket Expressions]
[Greedy and Lazy Match]

## Regex Components
***
### Anchor
A regular expression (regex) is a sequence of characters that is used to match a pattern in a bigger string. An email validation regex is used to check if a string is a valid email address or not. The email validation regex typically has two anchors, which are ^ and $. The ^ symbol is used to denote the beginning of a string, and the $ symbol is used to denote the end of a string. Therefore, when using an email validation regex to check for a valid email address, both the ^ and the $ symbols must be present for it to work correctly.

The caret (^) in the regex is used to ensure the entry includes something before the @ symbol. This way, a valid email address with a recognized domain (e.g. @gmail.com) is only accepted if something is provided before it so that the user cannot simply submit an @(domain).com email address.

The $ symbol is used in regular expressions to signify the end of an entire matching string. For example, if you wanted to match the end of a domain name in a URL, you could use the regular expression “.com$” to match all strings that end with “.com”. This can be used to match any domain that ends in the same way, such as “.net$,” “.org$,” or any other domain types. The use of the $ symbol indicates that any string that is matched has to end exactly with what comes after the symbol, which in the above example would be “.com.”

### Quantifiers
The + symbol is an overloaded symbol that is used as a quantifier in a regular expression. This quantifier indicates one or more of the preceding item. The {2,6} quantifier indicates there must be at least two, but not more than six of the preceding item. This regex allows for two to six of the preceding item that is specified and no more than six. This can be used to ensure that the input string meets a certain length or includes a specific number of certain words or characters.

Quantifiers are used to specify the number of characters a regular expression should match. For example, the regular expression /^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/ will look for a string of two to six alphabetic characters followed by a domain extension after an @ symbol. This regular expression ensures that only valid email addresses are accepted as valid input.

The + quantifier looks for one or more characters in astring. It matches the preceding expression 1 or more times. The * quantifier looks for 0 or more characters in a string. It matches the preceding expression 0 or more times. The ? quantifier looks for 0 or 1 characters in a string. It matches the preceding expression 0 or 1 times. The {n} quantifier looks for exactly n characters in a string. It matches the preceding expression exactly n times. The {a,b} quantifier looks for at least a characters, but no more than b characters in a string. It matches the preceding expression a or more times, but no more than b times.


The quantifier in this example: /^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/, is the plus sign (+). It indicates that one or more of the characters in the character class (defined by the square brackets) can be matched and the expression considered a valid match. The character class defines a range of characters, in this example lowercase letters (a-z), uppercase letters (A-Z), numbers (0-9), underscore (_), period (.) and hyphen (-). This character class allows us to match any combination of letters, numbers, underscores, periods and hyphens with a length of 2 to 6 characters.

### OR Operator
The | operator will match either of the patterns separated by it. For example, if you have the expression "dog|cat", it will match both "dog" and "cat". If used within a group, it will match any of the terms within the parentheses. If a range is used with |, it will match any of the characters in the range. Additionally, the order in which the patterns are tested matters. The first expression will be tried before the second, and if it does not match, the second expression will be matched.

### Character Classes
The \d within the second set of braces is a character class. Character classes are used in regular expressions to identify and match a range of characters within a given string. For example, the \d character class will match any single digit from 0 to 9. In the regex example provided, the \d character class is being used to search for a string which includes any single digit surrounded by two alphabetic characters.

**./^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/


The \D character class will match any character that is not a digit. \W will match any character that is not an alphanumeric character or underscore, and \S will match any character that is not a whitespace character. To use these character classes as inline modifiers, capital letter will be used, like \D, \W, and \S. The same is true for negating a character class, in which all cases must be capitalized.

### Flags
The multi-line flag in a regex is useful because it allows the expression to be across multiple lines without breaking it up. This is done by using the ^ symbol in the beginning, which signifies the start of a line and $ signifying the end of a line. By using this flag, an expression can be split up across multiple lines without requiring manual stitching together. This can make large expressions easier to read and understand.

### Grouping and Capturing
Paranteses are used for grouping is a way of annotating a regex expression to make it easier to read and understand. It uses parentheses to group together elements to allow for complex search and replacement operations. In this example, parentheses are used to group together meta characters, allowing literal characters to be searched for with greater precision. Grouping and capturing can also be used to isolate parts of a string so they can be back-referenced or replaced. This allows for more meaningful and powerful operations than would otherwise be possible.

**./^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/
**.([a-zA-Z0-9_.-]+) and ([\da-zA-Z.-]+) and ([a-zA-Z.]{2,6}) are all groups found in the regex above; the groups are for the NAME, DOMAIN, and EXTENSION of the given email address.

### Bracket Expressions
Bracket expressions are used in regular expressions to specify a set of characters to match. For example, in the regular expression used in this tutorial so far, the bracket expression [a-z] tells the regular expression to match any lowercase alphabetical character. Additionally, the expression [0-9] tells the regular expression to match any digit. Bracket expressions can also include ranges of character codes, such as [\u0000-\uFFFF] which matches any character in the Unicode character set.

.[a-zA-Z0-9_.-]

The characters that will match this bracket include lowercase letters (a-z), uppercase letters (A-Z), numbers (0-9), an underscore (_), a period (.), and a dash (-). These are the characters typically accepted in a wide range of programming languages and applications when defining variables or other identifiers. Other characters like !, @, #, $, %, ^, &, *, (, ), +, {, }, [, ], :, ;, <, >, ?, \, and | are usually not accepted in these brackets.

### Boundaries
No, boundaries are not usually required for email validation. The "@" symbol functions as a boundary and divides the address into its NAME, DOMAIN, and EXTENSION parts. As long as the address contains an "@" symbol, any other boundaries are unnecessary. Email validation only needs to check if the address is composed of valid parts and contains an "@" symbol in order to be valid.

### Back-references
Email validation does not require back references, as these are more typically used for HTML elements or for matching text between tags. Email validation can be performed simply by verifying the accuracy of the email address, such as making sure there is an @ symbol, a period and no invalid characters in the address. This is usually done using regex or search algorithms.

### References


## Author
***
I am currently a student attending the UCLA Web Development Coding Boot Camp.

Conatct me:
[GitHub](https://github.com/LatinLady)
