# Regex for beginners

Hello world! My name is Luc and I wrote up this document to give a brief overview of "Regular Expression" or commonly known as regex.

## Summary

I briefly described the bullet points in the table of contents with a short summary, characters you would use for each bullet point, and a code snippet example.

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
Code Snippet Example

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
Code Snippet Example

const regex = /go*d/;
console.log(regex.test('gd')); // Output: true
```

### OR Operator

The OR operator in regular expressions allows you to match either one pattern or another. It provides a way to specify alternative options within a regular expression. The OR operator is useful when you want to match multiple alternatives and any one of them can be considered a match. It provides a concise way to define multiple options within a single regular expression.

- | (Vertical Bar):

```
Code Snippet Example

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
Code Snippet Example

const regex = /[aeiou]/;
console.log(regex.test('Hello')); // Output: true
```

### Flags

Flags in regular expressions are optional parameters that modify the behavior of the regex pattern matching. They are appended to the end of the regex pattern and control how the matching process is performed. Here are some commonly used flags:

- g (global): Matches all occurrences.
- i (case-insensitive): Matches regardless of case.
- m (multiline): Matches across multiple lines.

```
Code Snippet Example

const regex = /hello/gi;
console.log('Hello, hello'.match(regex)); // Output: ['Hello', 'hello']
```

### Grouping and Capturing

Grouping and capturing are features used to organize and extract specific parts of a text pattern. They allow you to group multiple characters together and treat them as a single unit or capture their matched values for further use. You enclose characters or subpatterns with parentheses.

- () (parentheses): Groups patterns together and captures matched values.

```
Code Snippet Example

const regex = /(hello), (world)/;
const match = 'Hello, world'.match(regex);
console.log(match[1]); // Output: 'Hello'
console.log(match[2]); // Output: 'world'
```

### Bracket Expressions

Bracket expressions are a way to define a set or range of characters that you want to match against. They are specified by enclosing the desired characters inside square brackets "[]".

- [a-z]: Matches any lowercase letter.
- [A-Z]: Matches any uppercase letter.
- [0-9]: Matches any digit.
- [^0-9]: Matches any non-digit.

```
Code Snippet Example

const regex = /[a-zA-Z]/;
console.log(regex.test('Hello123')); // Output: true
```

### Greedy and Lazy Match

Greedy matching is used to match as much of the input string as possible while still satisfying the overall pattern. Greedy matching is useful when you want to capture the longest possible substring that matches a pattern.

Lazy matching is used to match as little as possible while still satisfying the overall pattern. Lazy matching is useful when you want to capture the shortest possible substring.

- Asterisk (*) - Matches zero or more occurrences of the preceding pattern.
- Plus (+) - Matches one or more occurrences of the preceding pattern.
- Question mark (?) - Matches zero or one occurrence of the preceding pattern. It is equivalent to {0,1}. 
- Curly braces ({m,n}) - Matches a specific range of occurrences of the preceding pattern. The values 'm' and 'n' represent the minimum and maximum number of occurrences.

- *? (lazy asterisk): Matches zero or more occurrences in a non-greedy manner.
- +? (lazy plus): Matches one or more occurrences in a non-greedy manner.
- ?? (lazy question mark): Matches zero or one occurrence in a non-greedy manner.

```
Code Snippet Example

const regex = /a.*?b/;
console.log('axbyb'.match(regex)); // Output: 'axb'
```

### Boundaries

Boundaries are special characters or assertions used to define specific positions in the text where matches should occur. They help in specifying the exact locations where patterns should start or end within a string.

- \b (word boundary): Matches a word boundary.
- \B (non-word boundary): Matches a non-word boundary.

```
Code Snippet Example

const regex = /\bworld\b/;
console.log(regex.test('Hello, world!')); // Output: true
```

### Back-references

Back-references allow you to refer back to previously matched groups within the pattern. They provide a way to reuse and manipulate captured text within the regex itself. 

- \1, \2, etc.: Matches a previously captured group.

```
Code Snippet Example

const regex = /(hello).*\1/;
console.log(regex.test('hellohello')); // Output: true
```

### Look-ahead and Look-behind

Look-Ahead (?=): Look-ahead assertions are denoted by "(?=)" and specify a condition that must be met after the current position in the text. They are used to match a pattern only if it is followed by another pattern.

Look-Behind (?<=): Look-behind assertions are denoted by "(?<=)" 
and specify a condition that must be met before the current 
position in the text. They are used to match a pattern only if it 
is preceded by another pattern.

```
Code Snippet Example

const positiveLookAheadPattern = /Hello(?=,)/;
console.log(text.match(positiveLookAheadPattern)); // Output: ['Hello']

const positiveLookBehindPattern = /(?<=,) World/;
console.log(text.match(positiveLookBehindPattern)); // Output: [', World']
```

## Author

I am a in training full-stack developer taking a bootcamp course through the University of Utah that used worked used to work for a tech company "Route" which ultimately inspired me to start my career in coding. I now work as an accountant for "Inspectre Solutions" which is a full service investigative and medical case management agency specializing in international worker’s compensation, Defense Base Act, war hazard claims. After I complete my coding bootcamp I intened on taking some time to sharpen my skills by doing projects for different coding languages before applying for junior developer jobs.
