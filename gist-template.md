# Regex or Regular Expressions Tutorial

In this tutorial, we'll  be going over  the characrters used in regular expressions and their given use.



## Summary

A regular expression(RegEx) is a sequence of characters that are often used as a search pattern to validate character combinations.


>*for instance in this example  tries to match any email adrress from the domain yahoo.com, hotmail, and gmail.com*
```
Regex example: (\W|^)[\w.\-]{0,25}@(yahoo|hotmail|gmail)\.com(\W|$)
```

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

# Regex Components

# Anchors

In order to understand anchors, first you must  know the way they operate for instance anchor do not match any character, instead anchor match a position. For instance 
the beginning of a string or the end.

- `^ `: The caret anchor matches the beginning of a string or line.

- `$ `: The dollar sign anchor matches the end of a String or line.

# Quantifiers

Quantifiers in regex determine the quantity of a character. Quantifiers are written in curly brackets{}. It counts how many times does a character appear in a string so that it matches the expression. Quantifiers can be considered either lazy or greedy.

- `*` Matches the previous element 0 or more times.
- `+` Matches the previous element 1 or more times.
- `?` Matches the previous element 0 0r  1 time.
-`{n}`Matches the previious element  exactly n  times.
- `{n,}` Matches the previous element n or more times.
- `{n,m}` Matches the previous element between n and m times.

# OR Operator
    
  The OR operator  In a regular expression it is expressed with a vertical character and allows you to compose regular expression patterns to match any one out of a set of alternative choices. 
    
# Character Classes

A character class is a group of characters that can be found within square brackets. It indentify the characters that will more than likely match a single character from a designated input string.

 - `\w `: matches any  character that is a letter(capital-lower case), number, or underscore.
 
 - `\W` : matches any character that is Not a letter(regardless of case) number, or underscore
 
 - `\d `: matches any character that is a number.
 
 - `\D `:  matches any character that is Not a digit 
 
 - `\s `: matches any  character that is a whitespace character such as: tabs,returns,spaces and form feeds
 
 - `\S `: matches any character that is Not a whitespace character.
 
 

# Flags

Flags are optional parameters that we can add to a plain expression to make it search in a different way. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behaviour.

- `i    Ignore Casing `:   Makes the expression search case-insensitively.

- `g    Global` :   Makes the expression search for all occurences.

- `s    Dot All `:   Makes the wild character . match newlines as well.

- `m    Multiline` :    Makes the boundary characters ^ and $ match the beginning and
                      ending of every single line instead of the beginning an ending of the whole string.
 
- `y    Sticky` :   Makes the expression start its searching from the index indicated in its lastIndex property.

- `u    Unicode `:    Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.

# Grouping and Capturing

Grouping and Capturing  are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (cat) creates a single group containing the letters "c" "a" and "t" 

# Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

# Greedy and Lazy Match
`'Greedy'` means match longest possible string.

`'Lazy'` means match shortest possible string.

# Boundaries
The `\b` is an anchor like the caret and the dollar sign. It matches at a position that is called a “word boundary”. This match is zero-length.


`\B` is the negated version of `\b`. `\B` matches at every position where `\b` does not. Effectively, `\B` matches at any position between two word characters as well as at any position between two non-word characters.

Since digits are considered to be word characters, `\b4\b` can be used to match a 4 that is not part of a larger number. So saying `\b` matches before and after an alphanumeric sequence is more exact than saying “before and after a word”.



# Back-references

Backreferences match the same text as previously matched by a capturing group. let's believe you want to match a pair of opening and closing HTML tags, and the text in between. By leveraging  the opening tag into a backreference, we can reuse the name of the tag for the closing tag.

>For Example: <([A-Z][0-9]*)\b[^>]*>.*?</\1> This regex contains only one pair of parentheses, which capture the string matched by [A-Z][0-9]*. 

This is the opening HTML tag. The backreference \1 references the first capturing group. \1 matches the exact same text that was matched by the first capturing group. The / before it is a literal character. It is simply the forward slash in the closing HTML tag that we are trying to match.

# Look-ahead and Look-behind
  Lookaheads and lookbehinds forces the main expressions to be what you have defined it as. Without it being exactly what it is it will not be accepted as a valid input. Lookahead and lookbehind are zero length assertions just like the start and end of line, and start and end of word anchors  The difference is that lookaround actually matches characters, but then gives up the match, returning only the result: match or no match. That is why they are called “assertions”. 

`(?=ABC)` is a postive lookahead and it matches a group after the main expression without including it in the result.

`(?!ABC)` is a negitive lookahead and it specifies a group that can not match after the main expression (if it matches, the result is discarded)

`(?<=ABC>)` is a postive lookbehind and matches a group before the main expression without including it in the result.

`(?<!ABC)` is a negitive lookbehind and Specifies a group that can not match before the main expression (if it matches, the result is discarded).

#


## Author

This tutorial was brought to you by [Jorman Israel](https://github.com/jisrael-R)

