# javascript-programming
javascript-programming

## Great quick ref

http://jsforcats.com/
book : eloquent javascript

The holy book:
https://github.com/getify/You-Dont-Know-JS/tree/master/up%20%26%20going
his website: getify.me
The good foundations.

The source code you write is not for the computer, its for a intermediary compiler...browser....etc
It's for you.

It has to make sense. For other developers.

Make it easy to process on the brain.

Syntax and grammmar tell you how to write javascript.

Syntax is like for english, there are punctuation marks, verbs, nouns, 
Grammar: Making a sentence(statement).

```
a = b * 2;

```

Single statement. Ends in ; meaning Im done. Sometimes not required. Use them when they make sense. Like end of operation.

Statement and expression:

```
(a = ((b) * (2)));
```

Identify exercise, below is expression value, values become statement:

```
((a) = ((b) * (2)) + ((foo)(c) * (3))));

```

OPERATOR PRECEDENCE!

# takes precedence!

Code can move backwards because of this. What is more precedent. 

To overwrite this multiplication, we can use parenthesis!


```
a = b * (2 + foo(c * 3));

```

Above we override precedence.

If we say

```
a = b + 2 *  foo(c * 3);

```

Now the second part takes precedence. We tweaked left to write processing.