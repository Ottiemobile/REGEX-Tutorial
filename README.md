# A Guide to Rejex



What is Rejex?
Regular Expression(otherwise known as Regex) is a sequence of characters that defines a search pattern for text. Regular expressions are commonly used to search for specific sequences of characters within a string, this could be used to extract specific information from any text such as phone numbers, email adresses, dates, and so forth. The most interesting thing about regular expressions is that it can be used in almost every programming language (Javascript, Java, Python, Ruby, etc.). Ever been on a search engine like Google or Bing? They use regular expressions in their search algorithm for people to find exactly what they're looking for.

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
  <img src="./assets/images/start-anchor.png" alt="Starting Anchor">
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


looking at the image above, when using this quantifier, users can grab  more than one 

A pretty neat feature, but what happens if you add another number on the other side of the comma?

Let's try typing teen{4,6} into the expression:
<br/>
<p align="center">
  <img src="./assets/images/quantifier-6.png" alt="This quantifier matches any piece of string with 4 or 6 of the last ">
</p>
<br/>

as shown above, the expression matches the similar string with 4 or 6 of the same last character in the string.

### OR Operator

OR Operators (also known as Alternation Operators) uses a boolean format to match a string that either has one piece of text or the other. for example:  

The OR operator being used below either matches a string with either b or c using a "(|)" method 

<br/>
<p align="center">
  <img src="./assets/images/or_operator1.png" alt="the OR Operator can match strings ">
</p>
<br/>

Surprisingly, it is not limited to just only two slots, you can add more slots for arguments to match more strings within the text area. 

<br/>
<p align="center">
  <img src="./assets/images/or_operator2.png" alt="the OR Operator can use two or more arguments within one regex request">
</p>
<br/>



### Character Classes
Character Classes asks the regex engine to find one specific key character class within a string, such as numbers, letters, and many others.


The `\d` expression can detect any digit within the string.

I created a couple of sentences using numbers inside the words to see if the regex expression can detect them, with no surprise, the expression spotted the numbers with ease. this is very useful if you want people to add numbers to a password like the one on the botom part of the image.

<br/>
<p align="center">
  <img src="./assets/images/cc1.png" alt="the \d function can detect any digit within a string">
</p>
<br/>

The `\w` expression can find any word character within a string, both alphanumeric and underscores.

<br/>
<p align="center">
  <img src="./assets/images/cc2.png" alt="the \w function can detect numbers and letters within a string as well as underscores.">
</p>
<br/>

looking at this image, we can see it is matching ONE character as a single match, it does not match one full word.

The `\s` expression can find any blank spaces within the text.


<br/>
<p align="center">
  <img src="./assets/images/cc3.png" alt="the \s function can match any peice of blank pieces of string within text">
</p>
<br/>


Using capital letter versions of these expressions can give you the opposite effect. 

The `\D` expression can match any single character that is NOT a number(NaN).
<br/>
<p align="center">
  <img src="./assets/images/cc4.png" alt="the \D function can match any single string that is not a digit">
</p>
<br/>


### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author
Ethan Torres is a web developer that is learning full-stack web development through the University of Texas at Austin.

check out his github to learn more about his past projects at:
https://github.com/Ottiemobile

