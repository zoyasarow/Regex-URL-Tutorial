# Regex Tutorial for URL Matching

A Regex (Regular Expression) is a computer science concept that represents a string of text or sequence of special characters that specify a search pattern. Regex's can be used to search for, represent & validate various text inputs, such as email addresses, passwords and URL's- which is what this tutorial will further explore!

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

One of the text inputs that Regex's can be used to validate are URL's. Below is the Regex we will explore:

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```

This seemingly random line of characters can be used to validate a URL. Let's get into it!

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

Out of the characters/symbols that make up regular expressions as representations text, Anchors are not used to match. Instead, they are used to mark the start and end of the Regex and are often represented by carrots (^) and dollar signs ($). They always follow the forward "/" and back "\" slashes that frame the Regex.

You can see the anchors in our URL regex below at the beginning "/^" and end "$/":

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```

Whatever immediately follows the anchors is what tells the Regex to look for at the beginning and end of the string. In our example, the regex will search for strings that begins with "https?:" and ends with a "?"

### Quantifiers

Quantifiers specify the number of occurrences for the Regex to match against. Each type of qualifier represent how many times its proceeding character/s will be searched for/matched against. Below are the different types of quantifiers:

    * "*" matches zero or more times
    * "+" matches one or more times
    * "?" matches zero or more times
    * "{n}" matches exactly n times
    * "{n,}" matches at least n times
    * "{n,m}" matches n to m times

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```

In our regex, the "?" is working to match the proceeding "https" zero or more times. The second "?" is working to match the proceeding (https?:\/\/) zero or more times. Same with the third "?" at the end of the regex working to match the proceeding "*\/".

In our regex, the "+" is working to match the proceeding "[\da-z\.-]" one or more times. 

There are also multiple asterisk's working to match their proceeding strings zero or more times, such as "[\/\w \.-]" and "([a-z\.]{2,6})([\/\w \.-]*)"

The regex is also working to match {2,6} between 2 to 6 occurrences of a string that contains any lowercase letter between a-z.

### Character Classes

Character classes are represented by a set of characters enclosed in brackets []. The character classes in our regex are

    * [\da-z\.-]
    * [a-z\.]
    * [\/\w \.-]

These represent the characters that will successfully match a single character from a given input string.   

### Flags

Flags change the search behavior of the regex. They are optional parameter's that modify its behavior of searching. Flags are represented by a single lowercase alphabetic character. There are 6 flags, listed below:

    * i (makes the expression search case-insensitively)
    * g (makes the expression search for all occurrences)
    * s (makes the wild character . match newlines)
    * m (makes the boundary characters match the beginning and end of every single line instead of the beginning and end of the entire string)
    * y (makes the expression start its searching from the index indicates in its lastIndex property)
    * u (makes the expression assume individual characters as code points versus code units)

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```   

In our regex, there are no flags that are influencing search behavior!     

### Grouping and Capturing

Capturing & grouping treats multiple characters in a regex as a single unit. These are represented by characters in parenthesis () that together will create an intentional string of text. In our regex, there are multiple capturing groups, including:

    * (https?:\/\/)
    * ([\da-z\.-]+)
    * ([a-z\.]{2,6})
    * ([\/\w \.-]*)

### Bracket Expressions

Similar to grouping, bracket expressions are multiple characters in a regex that are inside brackets that are used to match single characters in a list or a range of characters in a list. In our regex, there are multiple bracket expressions, check them out below!

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```  

### Greedy and Lazy Match

Greedy & Lazy matches are defined by how much or how little matching will be done. Greedy matches will try to match as much as possible and lazy matches will try to match as little as possible. Greedy matches are represented by plus signs (+) or quotation marks(""). For example, in our regex, the string of "[\da-z\.-]+" will try to be matched as much as possible.

Lazy matches can be represented by question marks (?)- there are multiple instances of lazy matches in our regex, both at the beginning and end.

### Boundaries

Boundaries (\b) is an anchor of sorts that define what can be matched to the left or the right of it's current position. The content/characters that exist between boundaries will be searched as whole words only. There are no word boundaries in our regex.

### Back-references

Back references are specified with a backslash and single digit (like \3) and match the proceeding text with a previous captured group/sub-expression. There are no back references in our regex!

### Look-ahead and Look-behind

Lookarounds (which include look-aheads and look-behinds) can be added before or after characters and access matching based on the type of look-ahead and look-behind (positive versus negative). If it is positive, then the characters (either left/behind or right/ahead) will match the phrase, and if it is negative,then they will not match.

    * (?=text) - positive look ahead
    * (?<=text) - positive look behind
    * (?!text) - negative look ahead
    * (?<!text) - negative look behind

There are not look-aheads or look-behinds in our regex!

## Author

Zoya (they/them) is a full-stack software developer in training who lives in Denver, Colorado

You can find them on Github at [@zoyasarow
](https://github.com/zoyasarow)
