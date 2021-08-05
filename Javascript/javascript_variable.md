# Introduction 

**Language is catagories in to two type**

| Static type | Dynamic type |
| ----------- | ------------ |
| In this type of language we have to complie befor run it | In this type of language we can declare a variable and run it |
| Ex:- c, c++, scala, rust etc | Ex:- javascript, python, ruby etc |

## About javascript 

* Javascript is client side scripting language.
* Javascript is created by Brendan Eich in 1995 and initially called as "Livescript". Later on it is maintain by a communtity/organization called as ECMA(created in 1997).
* It is used to programmantically perform action with in the page.
* Javascript can execute not only in the browser but also on the server. So we can use javascript client a well as a server side language.

# control structure 

| Control structure | Explanation | Syntax |
| ----------------- | ----------- | ------ |
| if else | if the given condition is true then statement of "if" block are executed otherwise "else" block statement is executed |if(condition){ statement; } else{ statement; } |
| for loop | Its given condition creates a loop that is executed as long as a condition is true. | for ( init; condition; increment ) { statement; } |
| while loop | Its given condition creates a loop that executes a block of code as long as the given condition evaluates to true. | while(condition){ statement; } |
| do-while loop | It check the condition at the end of loop. So,it executes the statements in the code block at least once even if the condition Fails. | do{ statement; }while(constion) |
| switch case | it will evaluate an expression against multiple possible cases and run one or more blocks of codes/statement base on matching case | switch (expression) {  case statement: break; case statement: break    default: statement } |

# Operator

### Arithmatics operator :-

| Operator | Explanation | Syntax |
| -------- | ----------- | ------ |
| + | Use for performing addition of numbers. |  a+b |
| + | It also used for concatenation in between strings | "a"+"b" = "ab" |
| - | Use for subtracting numbers. | a-b |
| * | Use for multiplication of numbers. | a*b |
| / | Use for division of numbers. | a/b |
| == | Gives true if the operands are equal. | a==b |
| === | Gives true if the operands are equal and of the same datatype. | a===b |
| !== | Gives true if operands of same type datatype but not equal. | a !== b |
| > | Gives true if the left operand is greater than the right operand. | a > b |
| >= | Gives true if the left operand is greater than or equal to the right operand. | a >= b |
| < | Gives true if the left operand is less than the right operand. | a < b |
| <= | Gives true if the left operand is less than or equal to the right operand. | a <= b |
| % | Gives the reminder of diviion operation | a % b |

### Logical operator :- 

| Operator | Explanation | Syntax |
| -------- | ----------- | ------ |
| && | It return false value if any one condition is false | a && b |
| OR | It return true value if any one condition is true | a  b |
| ! | It return reverse boolean value of given datatype | !a |

### Ternary operator :-

| Operator | Explanation | Syntax |
| -------- | ----------- | ------ |
| ?: | It is an alternative to the if else js statement. It creates a very small code of what an if else statement would take. | condition ? statement : statement |



# Variable & Datatype

* Variable is just like container,which holds the data or anything. In other words it allocate memory in the system.
* Data types basically specify what kind of data can be stored and manipulated within a programme.
* Datatype catagories into two type,
   * Primitive datatype
   * Non-primitive datatype

| Primitive datatype | Non-primitive datatype |
| ------------------ | ----------------------- |
| Primitives are stored by value | Non-Primitives are stored by reference.|
| It is bulit-in/pre-define data type | In this user have to define its type |
| It is immutable | It is mutable |
| Ex:- string,number,boolean,null,undefined,symbol(ES6) | Ex:- object,array,function |


* Primitive datatype
   * **string** - Anything enclose with "" is known as string.
   * **number** - Any mathematical number is known as number.
   * **boolean** - It has only two value either true or false.
   * **null** - In javascript null is a object and it value is zero.
   * **undefined** -  A variable that has not been assigned a value is of type undefined.

   * In javascript all values are divided into two type of value,
     * Falsy value(0) - blank string(""),undefined,null,number,NaN 
     * Truthy value(1) - All value are truthy value except falsy value.
     * Some exceptional concatenation values,
       * undefined+undefined = NaN 
       * undefined+null = NaN
       * undefined+number = NaN
       * undefined+"hello"(string) = undefinedhello

* Non-primitive datatype
  * **object** - object is a non-primitive data-type that allows you to store multiple collections of data in key value pair.
  * **array** - There is no such thing called array. Array is just a short version of object and index is a key, which we don't have to define.

# Scope 

* Scope means where you can access a specific variable or function in a code.
* Scope mainly divided into three categories
  * Global scope
  * Function scope/local scope
  * Block scope

### Global scope

* Any variable that’s not inside any function or block (a pair of curly braces), is inside the global scope.

Example :-

```javascript 
var message = "Hello Welcome"
function play() {
  console.log(message); // o/p will be "Hello Welcome"
}

play(); 

```
### Function scope/local scope

* Variables declared inside a function is inside the local scope. They can only be accessed from within that function, that means they can’t be accessed from the outside code

Example :-

```javascript
function play() {
  var message = "Hello Welcome";
  console.log(message) // o/p will be "Hello Welcome" 
}

play();
console.log(message) // o/p will be not defined

```
### Block Scope 

* Variable declared inside nearest pair of curly braces({}) is inside the block scope. They can only be accessed from within that pair of curly braces.It is introduced in ES6 version js so it is only applicable let,const but not for var.  

```javascript
{
  let message = "Hello Welcome";
  var name = "Rahul";
  console.log(message); // o/p will be "Hello Welcome"
}

console.log(message); // o/p will be not defined
console.log(name); // o/p will be "Rahul"

```

# Difference between var,let and const

| var | let | const |
| --- | --- | ----- |
| feature of ES5 | feature of ES6 | feature of ES6 |
| It can be re-declared | It cannot be re-declared | It cannot be re-declared |
| It can be reassigned | It can be reassigned | It cannot be reassigned | 

### var - 
How "var" acts in differnet scenario in javascript

```javascript
1. var a = 5;
var a = 10;
var b = 10
b=20
console.log(a) // o/p - 10
console.log(b) // o/p - 20

2. var message = "Hello world"
function play(){
  var message = "Welcome"
  console.log(message); // o/p- Welcome
}
play()
console.log(message); // o/p- Hello world

3. if(true){
  var message = "Hello world"
}
console.log(message); // o/p- Hello world

4. if(true){
  var message = "Welcome"
}
var message = "Hello world"
console.log(message) // o/p- Hello world 

```

### let -

How "let" acts in differnet scenario in javascript

```javascript
1. let a = 5;
let a = 10;
let b = 10
b=20
console.log(b) // o/p - 20
console.log(a) // o/p - cannot be re-declared

2. let message = "Hello world"
function play(){
  let message = "Welcome"
  console.log(message); // o/p- Welcome
}
play()
console.log(message); // o/p- Hello world

3. if(true){
  let message = "Hello world"
}
console.log(message); // o/p- variable is not defined

4. let message = "Hello world"
if(true){
  let message = "Welcome"
  console.log(message) // o/p - Welcome
}
console.log(message) // o/p- Hello world 

```
### const -

const is just act like "let" but cannot be re-assigned or re-intialized. But in case of object we can re-assigned it but cannot re-intialized.

```javascript
const a = 10
a=30
console.log(a) // o/p - Error

const b = 20
const b = 30
console.log(b) // o/p -  'b' has already been declared

```

# Copy by value and Copy by reference

## Copy by Value

* Javascript passes by value in case of primitive datatypes like Boolean, NULL, undefined, String, and Number. Here it copies the value of one variable into another. If we make any changes to the copied variable, it will not affect the original variable. Both the variables are independent of each other because they are pointing to two different memory locations.
```javascript
var a=10;
var b=a;
console.log(a); // o/p - 10
console.log(b); // o/p - 10
b=b+1;
console.log(a); // o/p - 10
console.log(b); // o/p - 11
```
* Explanation: Here the value of variable 'a' is assigned to variable 'b'. Even if we change the value of variable 'b', the value of variable 'a' will not change.

## Copy by reference

* Javascript passes by reference in case of non-primitive datatypes likes objects and arrays. Here if we change the value of copied variable then the value of original variable will also change because both the variables are refering to the same memory location.

```javascript
var original={
    name : "Rahul",
    hobby:["dance","reading"]
}
var copy=original;
console.log(original);  //  o/p - { name : 'Rahul', hobby: [ 'dance', 'reading' ] }
console.log(copy);  //  o/p - { name : 'Rahul', hobby: [ 'dance', 'reading' ] }
copy.hobby[1]= "painting"
console.log(original);  //  o/p -{ name : 'Rahul', hobby: [ 'dance', 'painting' ] }
console.log(copy);  //  o/p - { name : 'Rahul', hobby: [ 'dance', 'painting' ] }
```
* Explanation: The value of variable "original" is assigned to variable "copy".Here if we make any changes in the variable "copy" then the value of variable "original" will also change and vice versa.



```javascript
var original={
    name : "Rahul",
    hobby:["dance","reading"]
}
var hobbylist={
  one:"cooking"
};
var copy=hobbylist;
hobbylist.two=original.hobby;

console.log(original); //  o/p - { name : 'Rahul', hobby: [ 'dance', 'reading' ] }
console.log(hobbylist); //  o/p - { one: 'cooking', two: [ 'dance', 'reading' ] }

var copy=hobbylist;
original.name ={
  list:["Rahul","Babul"]
}
copy.two[1]="riding";

console.log(original); //  o/p - { name : { list: [ 'Rahul', 'Babul' ] },hobby: [ 'dance', 'riding' ]}
 
console.log(hobbylist); // o/p -{ one: 'cooking', two: [ 'dance', 'riding' ] }
console.log(copy); //  o/p - { one: 'cooking', two: [ 'dance', 'riding' ] }
```

* Explanation: Here changes made in the variable "copy" affects other two variables i.e., original and hobbylist.
