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

## Executing a program

  The javascript engine.

  ```
  a = 2;
  ```
  means give a the value of 2
  ```
  a = 2;
  becomes
  0101010100100101010101010010101

  ```

  ## Interpretation
  
  CPU is on line 1 now and doesn't know what's on line 2. 

  If you run

  ```
  a = 2;
  2();
  ```
  ERROR. Line 1 doesn't even really run because of the error on line 2. It always CATCHES at the beginningn and throws the error and breaks. Tnis is good thing, because you catch errors straight away rather than later all tangled.

  This mean JS is a compiled language.

  JS has both 

  error on runtime
  and error in code
  
  Usually cpu languages analyse everything then take action.

  errors in compiler phase: 3 =2; error.

  ## Can you run JS in command line?

  Node.js does this. E is for execute.

  ```
node -e "a = 2;"

  ```

Alert isn't defined by JS.

It's defined by the browser.

Node doesn't have alert. 

Developers use console.log(a);.

console log means what ever my last statement was, print it back.

Try this in the inspector:

```
var age = prompt("whatsup?");
undefined
console.log(age);
VM2164:1 ok

```

## ALL YOUR BASIC OPERATORS (AGAIN)

Assignment: = as in a = 2.
Math: + (addition), - (subtraction), * (multiplication), and / (division), as in a * 3.
Compound Assignment: +=, -=, *=, and /= are compound operators that combine a math operation with assignment, as in a += 2 (same as a = a + 2).
Increment/Decrement: ++ (increment), -- (decrement), as in a++ (similar to a = a + 1).
Object Property Access: . as in console.log().
Objects are values that hold other values at specific named locations called properties. obj.a means an object value called obj with a property of the name a. Properties can alternatively be accessed as obj["a"]. See Chapter 2.
Equality: == (loose-equals), === (strict-equals), != (loose not-equals), !== (strict not-equals), as in a == b.
See "Values & Types" and Chapter 2.
Comparison: < (less than), > (greater than), <= (less than or loose-equals), >= (greater than or loose-equals), as in a <= b.
See "Values & Types" and Chapter 2.
Logical: && (and), || (or), as in a || b that selects either a or b.

shortcut operator
```
a = a + 2;
a += 2;
```

Every variable should be formerly declared.

a = 42; is a bad idea.

this is better:

var a = 42;


the three ways to declare variables

const = a;
let = b;
var = c;

function d() {

}

## blocks

you can pair vars together to be reusable

```
{
var = a;
foo(a/2)
}
```

this block is standalone.

Some statements use the blocks

```

var b;

if (a > 10) {
    var a = 42;
    foo(a/2);
}
var c;

```

Is that statement true? yes, execute the block. Blocks also appear in functions.

```
var a = 42;

function foo() {
    var a = 10;
    bar(a / 2);
}
var c;
```

## Different function declarations

```
function foo() {} // function declaration

var bar = function(){} //function expression attached to a variable declaration
var bar = function baz() {}   //function expression attached to a variable declaration
```
the block is associated to a function and the block wont run unless you run the function

## conditional block statement

```

var a = 10;
if (a > 5) {
    a = a * 2;
}

```

Falsy values

"falsy"

0 
-0 
NaN
""
false
null
undefined


If it's not on this list it's true:

```
var a = 10;
if (a) {
    a = a * 2;
}
20
```

If a was 0 it would be a falsy value.

void means make everything after undefined.

```
void 42;
undefined
```

## Loops

```
if (a) {..}
// will di it until false
while (a > 10) {
}
//when the thing is false stop doing it
//for loop:
for  ( a = 5;  a < 10 ;  a++ ) {
console.log(a);
}
```

try this in browser:
```
for  (
         a = 5;  /*initialisation clause*/
         a < 10 ;  /*conditional clause*/
          a++ )  /*update clause*/
                        {
                console.log(a);
                }
```
5
6
7
8
9
undefined

```
for ( ; ; ) {}

```

# This will run forever because it has a condition that never FAILS

### break

```
while (true) {
    if (a >= 10) {
        break; /*break stops the loop*/
    }

}
```

this will run forever. we need an intialisation clause to tell it when to stop.

```
a=5;

while (true) {
    if {a>=10}{
        console.log(a);
        a=a+1;
    }
}
```

this is conceptually how all loops run. They run until they stop.

## functions
```
function foo(){
    a = a * 2;
    a = a + 3;
}
var a = 10;

foo();
console.log(a);
```

Be consistent if you want to keep all your vars at the top thats good.

```
function foo(b){/*b is a parameter, you can have multiple with comments.*/
    a = a * 2;
    a = a + b;
}
var a = 10;

foo(3);
console.log(a);
```

functions can also return values 

```
function foo(b){
    a = a * 2;
    a = a + b;
    return a / 2;
}
var a = 10;
var b = foo(3);
console.log(a);
console.log(b);
```
result 11.5 & 23
in es6, you can have default paramter values

# Returns in function

use return phoneCost * myTax not phoneCost = phoneCost * myTax


correct code 

```
const SPENDING_THRESHOLD = 200;
const TAX_RATE = 0.08;
const PHONE_PRICE = 99.99;
const ACCESSORY_PRICE = 9.99;

var bank_balance = 303.91;
var amount = 0;

function calculateTax(amount) {
	return amount * TAX_RATE;
}

function formatAmount(amount) {
	return "$" + amount.toFixed( 2 );
}

// keep buying phones while you still have money
while (amount < bank_balance) {
	// buy a new phone!
	amount = amount + PHONE_PRICE;

	// can we afford the accessory?
	if (amount < SPENDING_THRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

// don't forget to pay the government, too
amount = amount + calculateTax( amount );

console.log(
	"Your purchase: " + formatAmount( amount )
);
// Your purchase: $334.76

// can you actually afford this purchase?
if (amount > bank_balance) {
	console.log(
		"You can't afford this purchase. :("
	);
}
// You can't afford this purchase. :(
    ```