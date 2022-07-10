# Regex Helper

## Summary

A Regex Helper, or reuglar expression, is a pattern of special characters that define a search pattern and help manage text.

This is am example of a regex:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

- This string is for an email
- In the first section of the sting ([a-z0-9_\.-]+) the Regex is searching for character set with any lowercase letter,number (0-9),and characters(\_ . -) .
- Then the (+) is a quantifier that matches one or more of the proceeding tokens.
- The (@) marks a seperation between string searches and indicates the @ must be present for the email to fit the criteria.
- the second section ([\da-z\.-]+) the Regex is searching for (/d) or any digit (0-9)
- it also looks for all lower case letters(a-z) as well as characters(. -)
- Again the (+) is called to match one or more of the proceeding tokens.
- (\.) matches (.)
- Then the third section looks for all lowercase characters(a-z) and (.)
- {2,6} sets a minimum and maximum amoint of characters in the thris section.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character escapes](#character_escapes)
- [Character Classes](#character_classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping_and_capturing)
- [Bracket Expressions](#bracket_expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back_references)
- [Look-ahead and Look-behind](#look_ahead_and_look_behind)
- [Author](#author)

## Anchors

    Do not match any character. Rather, they match a position before or after characters
    ^  ( signifies a string that begins with the characters that allow. It can be an exact string or a range of possible expressions when displayed inside of bracket expressions)
    $ ( signifies a strings ending with characters that proceed it. )

## Quantifiers

    set the limits of the string that your regex matches. More than likely, they include the minimum and maximum number of characters that your regex is looking for, matching as many occurrences as possible.
    * Matches the pattern zero or more times
    + Matches the pattern one or more times
    ? Matches the pattern zero or one time
    {} Curly brackets can provide three different ways to set limits for a match:
    { x } Matches the pattern exactly x number of times
    { x, } Matches the pattern at least x number of times
    { x, y } Matches the pattern from a minimum of x number of times to a maximum of y number of times

## OR Operator

    ( | )  ex: (a|b|c)
    allows us to use the logic outside of bracket expression

## Character escapes

    ( \ )
    allows the regex to escape a character that otherwise would be interpreted literally.

## Character Classes

    .  Matches any character except the newline character (\n)

    \d   Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

    \w   Matches any alphanumeric character, including the underscore _ . This class is equivalent to the bracket expression [A-Za-z0-9_].

    \s   Matches a single whitespace character, including tabs and line breaks

## Flags

    the only exception where it does not need to be wrapped in slashes. Flags are placed at the end of a regex, after the second slash. Allows us to define additional functionality of the limits of that regex.

    g: Global search- tested against all possible matches in a string

    i: Case insensitive search

    m: multi line search - input string is treated as multiple lines6. Grouping and Capturing-

## Grouping and Capturing

    a way to treat multiple characters as a single unit.

    ex) if we are try to match (water), it creates single units of “w" "a" "t" "e" “r".

## Bracket Expressions

    Anything inside a set of square brackets ([]) represents a range of characters that we want to match. (Also known as positive character groups.).

    It's important to note that a bracket expression can be turned into a negative character group by adding the ^ symbol to the beginning of the expression inside the brackets.

    [] : anything inside the square brackets represents a range of characters that we want to match

## Greedy and Lazy Match

    A greedy quantifier always attempts to repeat the sub-pattern as many times as possible before exploring shorter matches by backtracking.
    Generally, a greedy pattern will match the longest possible string.
    By default, all quantifiers are greedy.
    A lazy (also called non-greedy or reluctant) quantifier always attempts to repeat the sub-pattern as few times as possible, before exploring longer matches by expansion.
    Generally, a lazy pattern will match the shortest possible string.
    To make quantifiers lazy, just append ? to the existing quantifier, e.g. +?, {0,5}?.

## Boundaries

    (\b)
    Boundaries determine what can be matched to the left and the right of the position

## Back-references

    refers to a previous part of the matched regex- these are specified with backslash and a single digit('\1'). This is used to match the same content as a previously matched subexpression11.

## Look-ahead and Look-behind

    commonly called “lookaround.” matches characters, but then gives up the match, returning only the result: match or no match. That is why they are called “assertions”. They do not consume characters in the string, but only assert whether a match is possible or not. This allows you to create regular expressions that are impossible to create without them.

    (?=foo) - Asserts that what immediately follows the current position in the string is foo

    (?<=foo) - Asserts that what immediately precedes the current position in the string is foo

    (?!foo) - Asserts that what immediately follows the current position in the string is not foo

    (?<!foo) - Asserts that what immediately precedes the current position in the string is not foo

## Author

- [Github Repo](https://github.com/jjtalamonti/regex_helper)
