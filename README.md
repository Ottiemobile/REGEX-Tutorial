# A Guide to Rejex

Introductory paragraph (replace this with your text)

What is Rejex?
Regular Expression(otherwise known as Regex) is a sequence of characters that defines a search pattern for text. Regular expressions are commonly used to search for specific sequences of characters within a string, this could be used to extract specific information from any text such as phone numbers, email adresses, dates, and so forth. The most interesting thing about regular expressions is that it can be used in almost every programming language (Javascript, Java, Python, Ruby, etc.)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Let's say that you want to make specific requirements for a user's password in order for it to be strong enough to be unguessable, so you would something something like this to your code: 

/^(?=.*[A-z])(?=.*[A-Z])(?=.*[0-9])(?=.*[*_%$@])(?!.*[pPoO])\S{6,}$/



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
Anchors are used to find specific matching words from either the begining of the sentence or the end of a sentence. 

the caret symbol (^) is used as the start anchor and it is used to match any piece of string that starts with the beginning word in a string: 

<br/>
<p align="center">
  <img src="./assets/img/start-anchor.png" alt="Starting Anchor">
</p>
<br/>

the dollar sign ($) is used as an ending anchor and it is used to match any piece of string that ends with the last word in the string:

<br/>
<p align="center">
  <img src="./assets/img/end-anchor.png" alt="Ending Anchor">
</p>
<br/>

Not typing in any specific type of anchor can locate specific pieces of text within the string 

<br/>
<p align="center">
  <img src="./assets/img/anywhere-anchor1.png" alt="Ending Anchor">
</p>
<br/>

<br/>
<p align="center">
  <img src="./assets/img/anywhere-anchor2.png" alt="Ending Anchor">
</p>
<br/>

### Quantifiers

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
