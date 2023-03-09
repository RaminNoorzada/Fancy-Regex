# Fancy Regex
This tutorial will explain how to use regular expressions to match random phone numbers in the format xxx-xx-xxxx. We will break down each component of the regex pattern /\d{3}-\d{2}-\d{4}/ and explain how it works.

## Prerequisites
Before we begin, you should have a basic understanding of regular expressions and their syntax. If you are new to regular expressions, you may want to review some introductory materials or tutorials before continuing.

## Regex Components
The regex pattern /\d{3}-\d{2}-\d{4}/ consists of the following components:

\d matches any digit character (0-9).
{3} specifies that the previous character (in this case, \d) should be matched exactly 3 times.
- matches a literal hyphen character.
{2} specifies that the previous character (again, \d) should be matched exactly 2 times.
{4} specifies that the previous character (yet again, \d) should be matched exactly 4 times.

## Usage
To use this regex pattern in your code, you can create a new RegExp object and pass in the pattern as a string:

```
const pattern = /\d{3}-\d{2}-\d{4}/;
// Or
const pattern = new RegExp('\\d{3}-\\d{2}-\\d{4}');
```
You can then use this pattern with string methods such as match() or test() to find or validate Social Security numbers in your input.

## Conclusion
Regular expressions can be a powerful tool for pattern matching and data validation. By understanding the components of a regex pattern and how they work together, you can create powerful patterns to match a wide range of input. We hope this tutorial has helped you better understand how to use regular expressions to match Social Security numbers.

## Quistions
Ramin Noorzada: https://github.com/RaminNoorzada 