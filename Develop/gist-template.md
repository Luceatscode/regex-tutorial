# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

Anchors are special characters used in regular expressions to match specific positions within a string. They do not match any actual characters, but represent positions in the text. Anchors are used to check that a pattern is found at a specific location in the input string.

- ^ (caret): Matches the start of a string.
- $ (dollar): Matches the end of a string.

```
const regex = /^Hello/;
console.log(regex.test('Hello, World!')); // Output: true
```
### Quantifiers

Quantifiers are metacharacters in regular expressions that specify the number of occurrences a pattern should match. They allow you to define the repetition or optional nature of a specific pattern.

- '*' (asterisk): Matches zero or more occurrences.
- '+' (plus): Matches one or more occurrences.
- ? (question mark): Matches zero or one occurrence.
- . (dot): Matches any character except a newline.

```
const regex = /go*d/;
console.log(regex.test('gd')); // Output: true
```

### OR Operator

The OR operator in regular expressions allows you to match either one pattern or another. It provides a way to specify alternative options within a regular expression. The OR operator is useful when you want to match multiple alternatives and any one of them can be considered a match. It provides a concise way to define multiple options within a single regular expression.

- | (Vertical Bar):

```
const regex = /cat|dog/;

console.log(regex.test('I have a cat')); // Output: true
console.log(regex.test('I love dogs')); // Output: true
console.log(regex.test('I own a horse')); // Output: false
```

### Character Classes

Character classes in regular expressions provide a way to match specific sets or ranges of characters. They allow you to define a group of characters that can be matched at a certain position in a string.

- [ ] (square brackets): Matches any character inside the brackets.
- [^ ] (caret within square brackets): Matches any character NOT inside the brackets.
- \d: Matches any digit.
- \w: Matches any alphanumeric character or underscore.
- \s: Matches any whitespace character.

```
const regex = /[aeiou]/;
console.log(regex.test('Hello')); // Output: true
```

### Flags

Flags in regular expressions are optional parameters that modify the behavior of the regex pattern matching. They are appended to the end of the regex pattern and control how the matching process is performed. Here are some commonly used flags:

- g (global): Matches all occurrences.
- i (case-insensitive): Matches regardless of case.
- m (multiline): Matches across multiple lines.

```
const regex = /hello/gi;
console.log('Hello, hello'.match(regex)); // Output: ['Hello', 'hello']
```

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
