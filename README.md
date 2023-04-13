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
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
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

In this specific regular expression, the OR operator is not used. Instead, a non-capturing group ``` (?:) ``` is used to match either of the two possible patterns separated by the "OR" operator.

### Character Classes

This Regex has one character class: ``` [a-z] ```.

This character class matches any lowercase letter from a to z. It is used to specify the allowable characters for the tag name in an HTML opening tag. Specifically, this expression matches a string that starts with ``` < ```, followed by one or more lowercase letters, captures zero or more characters that are not ``` > ``` using ``` [^>]+ ```, and possibly captures some characters enclosed between opening and closing tags having the same tag name.


### Grouping and Capturing

This Regex has both Grouping and Capturing

The first pair of parentheses ``` ([a-z]+) ``` creates a capturing group that matches one or more alphabetic characters that immediately follow the ``` < ``` character. This capturing group captures the tag name.

The first alternative ``` >(.*)<\/\1> ``` captures the contents of the HTML tag within the opening and closing tag. The text between the tags is captured by the second capturing group ``` (.*) ```.
The second alternative ``` \s+\/> ``` captures a self-closing tag that ends with a forward slash.

### Bracket Expressions

In this regex, we have a bracket expression ``` [^>]+ ``` which matches one or more occurrences of any character that is not ``` > ``` symbol. This bracket expression represents the attributes of an HTML tag that can include any character except for the closing ``` > ``` symbol.

The bracket expression ``` [a-z]+ ``` is also present in the regex, which matches one or more lowercase alphabetic characters that immediately follow the ``` < ``` character. This bracket expression represents the tag name of an HTML element.

The given regex has two bracket expressions that are used to match specific types of characters in the input string.


## Author

This Regex explanation was written by Paul D'Angelo Jr. You can visit my [GitHub](https://github.com/Pauldan1988) to see some of my repositories and work I have done personally and projects with other people.
