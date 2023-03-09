# Title (Fancy Regex) 'Reguler Expression

## Summary
I will be describing the regex pattern /\d{3}-\d{2}-\d{4}/, which is used to match a Social Security number in the format xxx-xx-xxxx. I will explain each component of the pattern and how it works to match this format.

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

Regex: [A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}

Exampl:
```
regex = r"[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}"
email = "example@example.com"
if re.match(regex, email):
    print("Valid email address")
else:
    print("Invalid email address")
```
## Anchors
Anchors
Anchors are used to match patterns that appear at the beginning or end of a line or word.

The caret (^) is used to match the beginning of a line. For example, the pattern ^hello will match "hello" only if it appears at the beginning of a line.
The dollar sign ($) is used to match the end of a line. For example, the pattern world$ will match "world" only if it appears at the end of a line.
Example:    
```

let text = "hello world\nhello everyone\nworld hello";
let pattern1 = /^hello/gm;
let pattern2 = /world$/gm;

console.log(text.match(pattern1)); // Output: ["hello", "hello"]
console.log(text.match(pattern2)); // Output: ["world", "hello"]
```
## Quantifiers
Quantifiers
Quantifiers are used to match patterns that occur a specific number of times.

The asterisk (*) is used to match zero or more occurrences of a pattern. For example, the pattern go*d will match "gd", "god", "good", "gooood", and so on.
The plus sign (+) is used to match one or more occurrences of a pattern. For example, the pattern go+d will match "god", "good", "gooood", and so on.
Example:
```
let text = "gd god good gooood";
let pattern1 = /go*d/g;
let pattern2 = /go+d/g;

console.log(text.match(pattern1)); // Output: ["gd", "god", "good", "gooood"]
console.log(text.match(pattern2)); // Output: ["god", "good", "gooood"]
```
## Grouping Constructs
Grouping Constructs
Grouping constructs are used to group patterns together and apply quantifiers or alternations to them as a group.

Parentheses () are used to group patterns together. For example, the pattern (ab)* will match zero or more occurrences of the string "ab".
The vertical bar (|) is used to match alternative patterns. For example, the pattern (dog|cat) will match either "dog" or "cat".
Example:
```
let text = "ab abab ababab dog cat";
let pattern1 = /(ab)*/g;
let pattern2 = /(dog|cat)/g;

console.log(text.match(pattern1)); // Output: ["ab", "abab", "ababab", ""]
console.log(text.match(pattern2)); // Output: ["dog", "cat"]
```
## Bracket Expressions
Bracket Expressions
Bracket expressions are used to match characters that belong to a specific set or range of characters.

Square brackets [] are used to match a single character from a set of characters. For example, the pattern [abc] will match "a", "b", or "c".
The caret (^) is used inside square brackets to match any character except those in the set. For example, the pattern [^abc] will match any character except "a", "b", or "c".
Example:
```
let text = "apple banana cherry";
let pattern1 = /[aeiou]/g;
let pattern2 = /[^aeiou]/g;

console.log(text.match(pattern1)); // Output: ["a", "e", "a", "a"]
console.log(text.match(pattern2)); // Output: ["p", "p", "l", " ", "b", "n", "n", " ", "c", "h", "r", "r", "y"]
```
## Character Classes
Character Escapes
Character escapes are used to match special characters or characters that have a special meaning in regex.

The backslash () escapes special characters or characters that have a special meaning in regex. For example, the pattern \$5 will match "$5".
The backslash followed by a letter or a sequence of digits matches a predefined character class. For example, the pattern \s matches any whitespace character, including space, tab, and newline.
Example:
```
let text = "Hello, world. How are you\\doing?";
let pattern1 = /\./g;
let pattern2 = /\\/g;

console.log(text.match(pattern1)); // Output: [".", "."]
console.log(text.match(pattern2)); // Output: ["\\"]
```
## The OR Operator
The OR Operator
The OR operator (|) is used to match either one pattern or another. It can be used to match alternative spellings or variations of a word.

The pipe (|) separates two alternative patterns. For example, the pattern cat|dog will match either "cat" or "dog".
Parentheses can be used to group the alternatives. For example, the pattern gray|grey is equivalent to (gray|grey).
Example:
```
let text = "I have a cat and a dog.";
let pattern = /cat|dog/g;

console.log(text.match(pattern)); // Output: ["cat", "dog"]
```
## Flags
Flags
Flags are used to modify the behavior of regular expressions.

The g flag is used to match all occurrences of a pattern in a string. For example, the pattern /a/g will match all occurrences of "a" in a string, not just the first one.
The i flag is used to perform a case-insensitive match. For example, the pattern /a/i will match both "a" and "A" in a string.
Example:

```
let text = "The quick brown fox jumps over the lazy dog.";
let pattern1 = /the/gi;
let pattern2 = /fox/g;

console.log(text.match(pattern1)); // Output: ["The", "the"]
console.log(text.match(pattern2)); // Output: ["fox"]
```
## Character Escapes
Character Escapes
Character escapes are used to match special characters or character sequences that have a specific meaning in regular expressions.

The backslash () is used to escape special characters or sequences. For example, the pattern \. will match a literal period (.), and the pattern \\ will match a literal backslash ().
Example:
```
let text = "Hello, world. How are you\\doing?";
let pattern1 = /\./g;
let pattern2 = /\\/g;

console.log(text.match(pattern1)); // Output: [".", "."]
console.log(text.match(pattern2)); // Output: ["\\"]
```
## Author
This regex totorial was written by Ramin Noorzada, a current Student of UC Davis Coding Bootcamp.
This assignment regex totorial was surprisingly intresting to me based on the requirment when I was stragling to find related material which luckily already was provided in the readme, I was able to find the required totorial expectations by navigating through out deferent resorces and many videos on the Inter-net wich then came along with some really importent information about the use and the imapct of the regex or 'Reguller Expreassion' in writting code. 

There for this was pretty imperesive assigment that I was able to acomplished.

Ramin Noorzada
https://github.com/RaminNoorzada 




