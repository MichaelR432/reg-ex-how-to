# A REGEX Tutorial Overview

Hi there! Ever heard the term REGEX? I am a new dev and this was a new concept to me. So I decided to make a tutorial explaining all the different REGEX values. Now both you and I can see/ use this resource. Below you will find a TOC that covers each REGEX expression I will describe and give examples to. 

## Summary

Regex stands for "Regular Expression" syntax. They are string values that represent a pattern used to patch some or all portions of a target string. There are many different variations and patterns of regex, so to be unique to their value, you will often see them made up of complex special characters. 

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
Anchors have a specific meaning in regex. They do not match any character but match the position before or after the character. There are two different types of anchors. 

 ^ – The caret anchor matches the beginning of the text.
 $ – The dollar anchor matches the end of the text.

 example | 
 ` let str = 'JavaScript'; `
 ` console.log(/^J/.test(str));`
 ` output = true `

 Above you are seeing the caret anchor reference the `first` position of the string value `Javascript` because the first value in the string is `J` the output is true.

 example | 
 ` let str = 'JavaScript'; `
 ` console.log(/t$/.test(str));`
 ` output = true `

 Above you are seeing the dollar anchor reference the `last` position of the string value `Javascript` because the last value in the string is `T` the output is true. 

 Other anchors are |

`\ Quote the next metacharacter`
`. Match any character (except newline)`
`| Alternation`
`() Grouping`
`[] Character class`

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string.

The simplest quantifier is a number in curly braces `{n}`. When you append the expression to the character class it specifies how many characters you want to match. 

example | 
`let str = 'ECMAScript 2020';`
`let re = /\d{4}/;`
`let result = str.match(re);`

`console.log(result);`

Output = `[2020]`

Above the expression `/\d{4}/;` matches a four digit number, so within that string it is searching for a number value with four numeric characters === 2020. 

Other quantifiers are |

`* Match zero or more times. `
`+ Match 1 or more times.`
`? Match zero or one time.`
`{ n, } Match at least a certain number amount of times. `
`{ n, m } Match the minimum and maximum amount of a certain number. `

### OR Operator

The or expression is represented by `||` or double pipes. You can use as many terms to compare as long as they are separated with the pipe character. They are often used as a Boolean comparison to represent true or false values. 

example | 

`const a = 3;`
`const b = 2;`

`console.log(a > 0 || b > 0);`
`output: true`

Above you are seeing the code expect the value of a `3` is greater than 0 or the value b `2` is greater than 0. Both statements equal the output true. 

### Character Classes

Character classes distinguish types of characters often distinguishing between letters and digits.

Other character classes are |

`\w Match a "word" character (alphanumeric plus "_")`
`\W Match a non-word character`
`\s Match a whitespace character`
`\S Match a non-whitespace character`
`\d Match a digit character`
`\D Match a non-digit character`

### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching. A flag is shown by using a single lowercase alphabetic character. There are six different flags. 

`i	Ignore Casing |	The expression will search case-insensitively.`
`g	Global | The expression will search for all occurrences.`
`s	Dot All | The wild character . match newlines as well.`
`m	Multiline | The boundary characters ^ and $  will match the beginning/ending of every single line instead of the beginning and ending of the whole string.`
`y	Sticky | The expression will start its searching from the index indicated in its lastIndex property.`
`u	Unicode | The expression will assume individual characters as code points, not code units, and thus match 32-bit characters as well.`

### Grouping and Capturing

Is a way of matching multiple characters as a single instance. The regex is placed inside a set of parentheses. 

`const path = 'posts/10';`
`const pattern = /(\w+)\/(\d+)/;`

`const match = path.match(pattern);`
`console.log(match);`

Above to capture both the resource (posts) and id (10) of the path (post/10), you use multiple capturing groups `/(\w+)\/(\d+)/`.

### Bracket Expressions

Brackets indicate a set of characters match. An individual character shown between the brackets will match.

`'donkey'.match(/[^abcd]/) // -> matches 'o'`

### Greedy and Lazy Match

'Greedy' expression will match longest possible string.

'Lazy' expression will match shortest possible string.

example |

`the greedy h.+l matches 'hell' in 'hello' but the lazy h.+?l matches 'hel'.`

### Boundaries

The expression for boundaries is \b. Matches the first character in a string, if it is a word character. It can match the last character in a string if it is a word character. 

example |

`in the string Hello, JS! the following positions qualify as a word boundary:`
`console.log('Hello, JS!'.match(/\bJS\b/)); // true`
`output= ["JS"]`

Above returns 'JS' because 'Hello, JS!' matches the regular expression /\bJS\b/:

### Back-references

Back-referencing means to reference a captured match, saved in memory, by a capturing group.

example |
`\2`

### Look-ahead and Look-behind

Expression matches for a pattern that are followed or preceded by another pattern. 

example |

`The syntax is: X(?=Y), it means "look for X, but match only if followed by Y". There may be any pattern instead of X and Y.`

## Author

Thanks again for reading. My name is Michael and I am a junior full stack developer. Feel free to connect with me on github https://github.com/MichaelR432. 
