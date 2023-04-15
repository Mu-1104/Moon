---
layout: post
title: "M's Regex Learning Log"
date: Starting from April 15th 2023
excerpt: "About Regular Expression"  
tags: [CS, LEARNING LOG, REGULAR EXPRESSION]
comments: true
---

# Resources

* [Regular Expressions Tutorial](https://www.regular-expressions.info/tutorial.html)

* [regex101](https://regex101.com/)

* [RegexOne:Learn Regular Expressions with simple, interactive exercises](https://regexone.com/)

* [RegexLearn](https://regexlearn.com/)

* [菜鸟：正则表达式教程](https://www.runoob.com/regexp/regexp-tutorial.html)

# Table of Contents

* Special Characters: including literal characters and 12 metacharacters

* Non-Printable Characters

# [Special Characters](https://www.regular-expressions.info/characters.html)

## Literal Characters

* `cat`: match cat in "About cats and dogs". This is like saying to the regex engine: find a c, immediately followed by an a, immediately followed by a t.

> Regex engines are case sensitive by default. cat does not match Cat, unless you tell the regex engine to ignore differences in case.

## Special Characters (metacharacters)

Metacharacters are special characters in regular expressions that have a predefined meaning and are used to define the rules for pattern matching. In regex, metacharacters are used to represent a set of characters, repetition, grouping, and more.

* the backslash `\`

  -  used to give special meaning to the character that follows it.
  
     - "\d": Matches any digit character (0-9).
  
     - "\w": Matches any word character (a-z, A-Z, 0-9, and underscore "_").
  
     - "\s": Matches any whitespace character (space, tab, newline, carriage return).

  - used to escape characters that would otherwise be interpreted as metacharacters.

* the caret `^`

  - When ^ appears at the beginning of a character set enclosed in square brackets ([ ]), it means negation. It matches any character that is not included in the set. 
  
    - For example, the pattern `[^aeiou]` matches any single character that is not a vowel.
  
  - When ^ appears at the beginning of a regular expression pattern, it means that the pattern must match at the beginning of the string being searched.
  
    - For example, the pattern `^hello` matches the string hello world, but not world hello.

* the dollar sign `$`
  
  - used to match the end of a line or string. 
  
    - For example, the pattern `world$` matches the string hello world, but not world hello.

* the period or dot `.`
  
  - matches any single character except for a newline character. 
  
    - For example, the regex `b.t` matches the strings "bat", "bet", and "bit", but not "b\n\rt" because the newline character is not matched by the '.'.

* the vertical bar or pipe symbol `|`

  - used to indicate alternation or a logical OR between multiple patterns. The | operator matches either the pattern to the left or the pattern to the right of the operator. 
  
    - For example, the regex `cat|dog` matches either "cat" or "dog". The regex `(cat|dog) food` matches either "cat food" or "dog food".

* the question mark `?`
  
  - indicates optional characters or groups. The ? operator matches zero or one occurrences of the preceding character or group. 
  
    - For example, the regex  `colou?r` matches either "color" or "colour". 
  
  - You can also use the ? operator to make other metacharacters optional, such as the + and * operators. 
  
    - For example, the regex `a+?` matches zero or more occurrences of the character "a", but matches the minimum number of characters possible.

* the asterisk or star `*`
  
  - indicates zero or more occurrences of the preceding character or group. 
  
    - For example, the regex `ab*` matches "a", "ab", "abb", "abbb", and so on.

* the plus sign `+`
  
  - indicates one or more occurrences of the preceding character or group.
  
    - For example, the regex `ab+` matches "ab", "abb", "abbb", and so on, but not "a".
  
  - Keep in mind that the + operator matches the maximum number of characters possible. If you want to match the minimum number of characters possible, you can use the +? operator instead.
  
    - The regex `go+?d` matches "god" and "good", but not "gooood".
  
    - The regex `a+?b` matches one or more "a" characters followed by a single "b".
  
* the opening parenthesis `(`
  
  - used to create a capturing group. A capturing group is a way to group a subpattern together and capture the matched text so that it can be referenced later.
  
    - For example, the regex `(abc)+` matches one or more occurrences of the group "abc", and captures the matched text in a group. You can then reference the captured text later in your regex or in your code.

    - The regex `(\d{3})-\d{4}` matches a string that contains a hyphen-separated US phone number, such as "123-4567", and captures the three-digit area code in a group.
  
    - The regex `(hello|hi|hey)` there matches "hello there", "hi there", or "hey there", and captures the greeting in a group.

  - You can also use non-capturing groups by using the `?:` syntax. A non-capturing group is a way to group a subpattern together without capturing the matched text.
  
    - The regex `(?:\d{3})-\d{4}` matches a string that contains a hyphen-separated US phone number, such as "123-4567", but does not capture the three-digit area code in a group.
  
    - The regex `(?:Mr\.|Ms\.|Mrs\.) [A-Z][a-z]+` matches a string that contains a person's name with a title, such as "Mr. Smith" or "Mrs. Johnson", but does not capture the title in a group.

* the closing parenthesis `)`
  
  - used to close a capturing or non-capturing group.
  
  - A capturing group is created by placing one or more subpatterns inside opening and closing parentheses. The group can then be referenced later using a backreference or by accessing the matched text directly.
  
    - For example, the regex `(\d{3})-(\d{4})` matches a hyphen-separated US phone number, such as "123-4567", and captures the area code in the first group and the local number in the second group. You can then reference the captured groups later in your regex or in your code.
  
    - The regex `(\w+)\s+(\w+)` matches two words separated by one or more spaces, and captures each word in a separate group.
  
  - A non-capturing group is created by placing one or more subpatterns inside opening and closing parentheses, and then adding the ?: syntax immediately after the opening parenthesis. The group can be used to group subpatterns together without capturing the matched text.
  
    - For example, the regex `(?:Mr\.|Ms\.|Mrs\.) [A-Z][a-z]+` matches a person's name with a title, such as "Mr. Smith" or "Mrs. Johnson", but does not capture the title in a group.
  
* the opening square bracket `[`
  
  - used to create a character class. A character class is a way to match a set of characters within a single position in the regular expression.
  
    - For example, the regex `[aeiou]` matches any vowel character, and can be used to match words that contain any of those vowel characters.
    - The regex `[A-Za-z]+` matches any alphabetical word, regardless of case.

  - use character ranges in a character class by using a hyphen - between two characters.
  - For example, the regex `[a-z]` matches any lowercase letter, and the regex `[A-Za-z]` matches any alphabetical character regardless of case.

* the opening curly brace `{` 
  
  - used to create a quantifier that matches a specific number of occurrences of the preceding character or group.
    
    - For example, the regex `a{3}` matches three consecutive "a" characters, and the regex (abc){2} matches two consecutive occurrences of the group "abc". It matches "abcabc", "xyzabcabc123", but not "abc" or "abcaabc".

  - You can also use the curly braces to specify a range of occurrences, such as {2,4}, which matches two to four occurrences, or {3,}, which matches three or more occurrences.
    
    - The regex x{3,6} matches any string of three to six consecutive "x" characters.
  
    - The regex (abc){2,} matches two or more consecutive occurrences of the group "abc".
  
    - The regex \d{2,4} matches any string of two to four digits.

> If you want to use any of these characters as a literal in a regex, you need to escape them with a backslash. If you want to match 1+1=2, the correct regex is 1\+1=2. Otherwise, the plus sign has a special meaning.
> 
> Note that 1+1=2, with the backslash omitted, is a valid regex. So you won’t get an error message. But it doesn’t match 1+1=2. It would match 111=2 in 123+111=234, due to the special meaning of the plus character.

# [Non-Printable Characters](https://www.regular-expressions.info/nonprint.html)

Non-printable characters are characters that cannot be displayed visibly or have special meanings in the context of the text or the system that processes it. In regular expressions, non-printable characters can be represented by escape sequences or special metacharacters.


# Learning Log

| DATE	| ACTIVITIES | DURATION | COMPLETION STATUS | TOTAL OCCURRENCES |
| :----: | :----: | :----: | :----: | :----:|
| 2023-04-15| [Literal Characters and Special Characters](https://www.regular-expressions.info/characters.html) | 2h | done | 1 |

