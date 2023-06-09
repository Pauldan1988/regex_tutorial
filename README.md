# Reg-Existing
___
Regex, short for Regular Expression, is a sequence of characters that forms a search pattern. It's used mainly in string matching and manipulation by searching for specific patterns within a larger text. These patterns can be anything from simple alphabets, numbers or special characters, to complex expressions used to validate, clean or extract data. In programming, regex is widely used in scripting languages, text editors, and other tools to perform advanced string manipulation and pattern matching operations.

## Summary
___

Here is an example of a regex that matches HTML tags:

``` /^<([a-z]+)([^>]+)*(?:>(.*)<\/\1>|\s+\/>)$/ ```

This regular expression can be used to easily extract HTML tags and their attributes from a larger block of text, such as an HTML file. It allows for flexibility in the formatting of tags and their attributes, making it easier to handle edge cases that may arise. By using this regex, one can quickly parse through an HTML file and extract only the relevant tags or attributes.

## Table of Contents

- [Reg-Existing](#reg-existing)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
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
  - [Author](#author)

## Regex Components

* Here's a breakdown of the components in this regular expression:

* ``` ^ ``` - matches the start of the string.

* ``` <([a-z]+) ``` - matches an opening angle bracket < followed by one or more lowercase letters (captured as the first group using parentheses).

* ``` ([^>]+)* ``` - matches zero or more characters that are not angle brackets (captured as the second group).

* ``` (?:> ``` - starts a non-capturing group for the ending angle bracket > followed by either:

* ``` (.*)<\/\1> ``` - any number of characters (captured as the third group) followed by a closing tag with the same name as the opening tag (using the backreference \1 to refer to the captured text from the first group).

* ``` |\s+\/>) ``` - or one or more whitespace characters followed by a self-closing tag />.

* ``` $ ``` - matches the end of the string.

### Anchors
This regex has two types of anchors:

``` ^ ``` - The caret symbol indicates the start of a line. In this regex it is used to match HTML tags that are at the beginning of a new line.

``` $ ``` - The dollar sign indicates the end of a line. In this regex, it is used to ensure that the entire tag or attribute is matched until the end of a line.

These anchors are important as they allow us to accurately match only the specific HTML tags and attributes we are looking for, without any extraneous characters or information.

### Quantifiers

This regular expression contains several quantifiers. The ``` + ``` quantifier is used to match one or more lowercase letters within angle brackets. The ``` * ``` quantifier matches zero or more characters that are not the ``` > ``` character. The ``` ? ``` quantifier makes the ``` (?:) ``` group optional. The ``` * ``` quantifier matches zero or more whitespace characters before a closing self-closing tag. Finally, the . period character matches any non-newline character and the ``` * ``` quantifier is used to match zero or more of these non-newline characters.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
