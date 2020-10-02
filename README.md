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
  <img src="./assets/images/end-anchor.png" alt="Ending Anchor">
</p>
<br/>

Not typing in any specific type of anchor can locate specific pieces of text within the string:

<br/>
<p align="center">
  <img src="./assets/images/anywhere-anchor1.png" alt="An Anchor with no specifc location symbol">
</p>
<br/>
Looking at this image, you can see that "there" was located in the middle of the string with no use of the "$" or "^" symbols, making it focus on finding the specific piece of text anywhere on the 


<br/>
<p align="center">
  <img src="./assets/images/anywhere-anchor2.png" alt="Another Anchor with no specifc location symbol">
</p>
<br/>

reminder that these expressions are case sensitive

### Quantifiers
The Quantifier element matches the following piece of text one or more times.

The star symbol (*) is used to match text within a string that has a specific piece of text with none or more 
of the last string text:

<br/>
<p align="center">
  <img src="./assets/images/quantifier-1.png" alt="The quantifier that uses the * symbol to find a specific peice of text with or without the last character in the expression. ">
</p>
<br/>

The plus symbol (+) finds and matches text within the string followed by one or more of the same last character:

<br/>
<p align="center">
  <img src="./assets/images/quantifier-2.png" alt="The quantifier that uses the + symbol to find one or more of the last character in the piece of string.">
</p>
<br/>

The question mark (?) matches text in a string followed by either no or one of the last character in a piece of text.

<br/>
<p align="center">
  <img src="./assets/images/quantifier-3.png" alt="The quantifier grabs pieces of string within a text that either uses no or one of the last character.">
</p>
<br/>

Looking at this image, you can see that the expression still grabbed all or only a part of the strings that contained "ab" and/or "c" within the text.

The curly brackets "{}", is able to match in multiple ways:

using curly brackets with only one number inside like this can match a string that has matching string followed by the exact number of last specific piece of a matching character.

For example: the expression {4} will find any piece of string that has exactly 4 of the same last character on that said text.   

<br/>
<p align="center">
  <img src="./assets/images/quantifier-4.png" alt="This quantifier grabs any piece of string that matches as well as having a specific number of 'n''s given within the brackets.">
</p>
<br/>

If you have a comma after the number within the curly brackets like this: {4, } , you are then finding the matching text as well as 4 or more of the same character.

<br/>
<p align="center">
  <img src="./assets/images/quantifier-5.png" alt="This quantifier grabs any piece of string that matches as well as having a specific number of 'n''s given within the brackets.">
</p>
<br/>


loooking at the 


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
Ethan Torres is a web developer that is learning full-stack web development through the University of Texas at Austin.


<br/>
<h2 align="center">
  Click <a href:"https://github.com/Ottiemobile">HERE</a> to learn more about his past projects.
</h2>
<br/>