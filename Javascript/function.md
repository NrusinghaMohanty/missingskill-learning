
# Function

### What is function ?

* Block of code written to do a particular take is calld as "function". It just acts like a variable.
* Some properties of function
  * Hoisted
  * Scope
  * Overwrite
  * Act like a container(object)
* Function is a first class citizen that means it can do anthing in javascript. It can access everything in javascript. It can assign to a variable,declare to a variable and return as function also.

```javascript
var message = "hello world"
function print(){
    console.log(message)
}
print() // hello world

```
N.B - ` !!functionName && (typeOf functionName === "function") && functionName `

* It is used a checkpoint. We can use it to prevent error.
* Here, 
  * !!functionName - To ensure that functionName is defined or not.
  * typeOf functionName === "function" - To ensure that functionName is actually a function or not.
  * functionName - After all the above check functionName will b executed.

# How function acts in different scenarios

1. **How it acts in the case of var and let**

```javascript
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

```javascript
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
```javascript
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

```javascript
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

6. **Cascade function/Function chaining**

```javascript
var print = function(){
    var innerOne = function(){
      var innerTwo= function(fun){
        console.log(fun)
        return "inner two value"
      }
      console.log("inner one value")
      return innerTwo
    }
    return innerOne

}

var result = print()()("Inside function")

//0/p - "inner one value"
 // "Inside function"
 // "inner two value" 

```

# Higher-order function

* Any function that take function as a paramter or return a function or both is known as "higher-order function".

```javascript
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

```javascript
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

# Immediately invoked function(IIFE)/Self executing function(SEF)

```javascript
(function(){
    const sayHello = 'Hello';
    console.log(sayHello);
})();   // o/p sayHello


const language = "Javascript";
(function print(param){
    console.log(param);
})(language)   // o/p Javascript

```
* The anonymous function above will be invoked right after it has been defined. The benefit of self-invoking functions is that they enable us to execute code once without cluttering the global namespace.

# Inline function 

* It is passed directly as an agrument/parameter to another function.

```javascript
function play(message, name) {
  message(name);
}

play(function print(item) {
  console.log("Name " + item);
}, "Rahul"); // "Name Rahul"

```

# Arrow function

* Arrow function in JavaScript is a simpler way of writing functions. Arrow function was introduced in ES6 and provides short and easy way to write functions in the JavaScript. They utilize a new token => that looks like a fat arrow , So it also called is the Fat arrow function . Arrow function are always anonymous that means it has no name.

```javascript
var example = function() {  // Normal function
return "welcome";
}

var example = () => { // Arrow function
return “welcome”;
}

```

# Prototype Constructor

* In javascript function can be converted into a object. Prototype is an implantation of class structure.prototype itself is a object while a constructor is a pointer to the function that created the object. A constructor is a pointer.

**How to create a object prototype from a function**
```javascript
function Person(name){
    console.log(name)
}
var value = new Person(); // In here value is Object
Person("babul") 
```

```javascript
function Person(name,age){
    this.name = name;
    this.age = age
}
var value = new Person("babul",24)
var value2 = new Person("harish",25)
console.log(value.name,value.age) // babul 24
console.log(value2.name,value2.age) // harish 25
```

**How can we attach a method to any object contructor**

```javascript
Person.prototype.getName = function(){
    return this.name
}
console.log(value.getName(),value2.getName()) // babul harish
// Here this keyword refer to the object(value,value2 from above example)
```
**object literal**
```javascript
var obj = { name: "babul", age: 24} // It is a object literal

// internally js do is
 var Obj = Object(name,age){
        this.name= name
        this.age= age
}
var obj = new Obj()
```