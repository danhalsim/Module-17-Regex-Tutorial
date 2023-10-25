# GitHub Gist

https://gist.github.com/danhalsim/218c6615b30df95a927bb008284cea06


# Regex Tutorial: Matching a Hex Value

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. This tutorial will teach you how to use a regex to match and validate hexadecimal color codes.

## Summary

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This regex checks if the text begins with the "#" symbol. In HTML and CSS, colors often start with "#," but this "#" is not mandatory. So, it can be there or not. The ? means it's optional.

After the "#," it looks for either 6 characters or 3 characters. These characters must be a combination of numbers (0-9) and letters (a-f), and it doesn't matter if the letters are in uppercase or lowercase. This is the actual color code.

Finally, it checks that the color code should go all the way to the end of the text. It shouldn't be part of a longer word or phrase.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors

The `^` symbol signifies the beginning of the input string. `$` signifies the end of the string.

### Quantifiers

`?` specifies that the following character or group (the `#` in this case) can occur once or zero times. This means the `#` is optional; hex color codes can start with one or not.

`{}` specifies the exact number the preceding character class or group should be repeated. In this regex, one side of the OR operator specifies that there must be 6 hexadecimal characters in a row. The other side specifies 3.

### Grouping Constructs

`()` are used for grouping. A group of characters is treated as a single unit. In this regex, this grouping encompasses bracket expression and the OR operator.

### Bracket Expressions

`[]` are used to define a character class. The next section will explain its use in this regex.

### Character Classes

`a-f` matches any lowercase letter. `0-9` matches any digit. The hex color code must contain these values.

### The OR Operator

`|` acts as an OR operator. In this regex, it separates two alternative patterns: `[a-f0-9]{6}` and `[a-f0-9]{3}`.

## Author

Hi, my name is Daniel! I'm a student in UCI Coding Bootcamp and I love learning to code and learning about coding.

Visit my GitHub here: https://github.com/danhalsim