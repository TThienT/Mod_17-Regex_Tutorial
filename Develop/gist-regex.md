# Mod_17-Regex_Tutorial

Regex, which stands for regular expression, is essentially a type of text string that helps us create patterns to find and handle specific text in a more efficient way. Let's take an example to understand it better. When we use the "ctrl + F" shortcut to search for specific words or numbers in the VS code text editor, we can find a button labeled ".*" on the right-hand side, which allows us to perform searches using regex. In simpler terms, regex enables us to define patterns and locate specific text more effectively.

## Summary

In this tutorial, we're going to learn about using regex to match email addresses for verification purposes. The specific regex expression we'll be using is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. Some examples of email addresses that fit this format are FirstName.LastName@google.com or myemail@yahoo.com, and so on. We'll break down the different parts of the regular expression and explain what they do.

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
   In the email snippet, the ^ symbol indicates the beginning of the email, and ([a-z0-9_\.-]+) is the pattern that the email should start with. Similarly, the $ symbol represents the end of the email, and ([a-z\.]{2,6}) is the pattern that the email should end with.

### Quantifiers 
   - The asterisk (*) means one or more occurrences of "cde," where "cde" can be followed by zero or more "e" (e.g., "cde," "cdee," "cdeee," etc.).
   - The plus sign (+) also means one or more occurrences of "cde," with the same condition as the asterisk.
   - The question mark (?) indicates zero or one occurrence of "cde," so it can match both "cd" and "cde" (e.g., "cd," "cde").
   - The curly braces ({}) are used to specify a specific number of occurrences. For example, "cde{2}" means "cdee" will match, but not "cde" or "cdeee."
### OR Operator
   In academic terms, the symbol "|" indicates "or." So, if we have "abc|xyz," it means that either "abc" or "xyz" can be a match. Similarly, the symbol "[]" works in the same way.

### Character Classes
   \d matches a single digit character. 
   \w matches a single word character, regardless of whether it's a letter or a digit.
   \s matches a single white space character. 
   . matches any character.

### Flags
   The "/" flag creates a regex. It appears at the start and end for matching email regex. It's also seen in the search bar for regex searches. "/g" means global search and returns all matches.

### Grouping and Capturing
   The parentheses () create a group to capture specific matches. For instance, in the pattern c(ba), only the string cba will match. The position of the match within a larger string, like fdsdcbasfdsf, doesn't affect it.

   On the other hand, the ?: disables capturing for a group. In the pattern a(?:bc), both abc and a will match without capturing the group.

### Bracket Expressions
   When using brackets, [abc] matches any of the letters a, b, or c. It can also be written as a|b|c. [a-c] is the same as the previous expression. [a-fA-F0-9] matches any letter from a to f (both lowercase and uppercase) and any digit from 0 to 9. [^a-zA-Z] matches 
   any character that is not a letter from a to z or A to Z.

### Greedy and Lazy Match
   Greedy search is when quantifiers (*, +, {}) expand the match as much as possible in the given text, aiming for the longest string match.

   Lazy search, on the other hand, uses the ? symbol. For example, /".+?"/g is used to match any characters between double quotation marks. In the sentence "Coding is fun," only the word "Coding" within the quotation marks would be searched.
### Boundaries
   The symbol \b is used to search for whole words. For instance, if we search for \bapple\b, only the word "apple" will be matched, and not "greenapple" or "redapple".

### Back-references
   ([abc])\1 matches consecutive characters of the same letter in the group [abc]. For instance, it finds patterns like aa, aaaaaa, bb, bbbbbb, and cc, cccccc without any restriction on the number of repeating letters.

### Look-ahead and Look-behind
   The pattern "d(?=g)" matches only "d" followed by "g" without including the "g" in the match. Similarly, "(?<=f)g" matches only "g" preceded by "f" without including the "f" in the match.

## Author

My Contact: https://github.com/TThienT/Mod_17-Regex_Tutorial.git


