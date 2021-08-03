
# Function

### What is function ?

* Block of code written to do a particular take is calld as "function". It just acts like a variable.
* Some properties of function
  * Hoisted
  * Scope
  * Overwrite
  * Act like a container
  * Object
* Function is a first class citizen that means it can do anthing in javascript. It can access everything in javascript. It can assign to a variable,declare to a variable and return as function also.

```
var message = "hello world"
function print(){
    console.log(message)
}
print() // hello world

```

# How function acts in different scenarios

1. **How it acts in the case of var and let**

```
function print(){
    console.log(message)
}

print()
var message = "hello world" // undefined

function print(){
    console.log(message)
}

print()
let message = "hello world" // Cannot access 'message' before initialization

```
2. **Declaration and assignment function**

```
// function declaration
print()
function print(){
    console.log(message) 
}

// function assignment
print()
var print = function(){   // function which has no name is called as anonymous function. 
    console.log(message) // o/p will be error
}

```
Explanation : In the function declaration we can call the function before declaring it because function is an independent entity and can be hoisted. But in case of function assignment we cannot call the function before declaring it because we assigned it to a variable and variable declaration is hoisted not assignment. 


4. **Function returning a function** 
```
function outerOne(param){
    var innerOne = function(param){
        console.log(param);
        return "xyz"
    }
   return innerOne; 
}
var functionOne = outerOne("Hello")
var functionTwo = functionOne("welcome")  // o/p- welcome
console.log(functionTwo) // o/p - xyz

```
Explanation : Here functionOne contains the function innerOne(return by outerOne). functionTwo contains the value of return by innerOne that is "xyz" .

5. **Function pass as a parameter/reference**

```
var printOne = function(item){
    console.log(item)
}
var printTwo = function(param){
    var a = 10;
    var b = 20;
    var c = a*b;
    param(c)
}

printTwo(printOne) // o/p - 200

```
Explanation : Here function printOne passed as a parameter to printTwo in other words, param is actually the function assigned to printOne.

# Higher-order function

* Any function that take function as a paramter or return a function or both is known as "higher-order function".

```
var printOne = function(item){
    console.log(item)
}
var printTwo = function(param){
    var a = 10;
    var b = 20;
    var c = a*b;
    var innerOne = function(){
        console.log("item")
      return "Hello"
    }
    param(c)
    return innerOne

}

var one = printTwo(printOne) 
var two = one()
console.log(two) 

// o/p - 200
"item"
"Hello"
```

# Pure function

* The function which doesn't modifiy the value of parameter or the value passed to the function is known as "Pure function".
* It can change the local variables.

```
var value = 5;
function print(item) {
    return item + 2 + 3;
}
print(value)  // pure function

var value = 5;
function print(item) {
    value = 10
    return item + 2 + 3;
}
print(value) // immpure function

```
