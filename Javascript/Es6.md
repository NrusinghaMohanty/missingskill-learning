
# setTimeout()

* setTimeout() run the function once after the given interval of time.

```javascript
function print(){
    console.log("hello world")
}
setTimeout(print,5000) // print "hello world" after 5sec
```
```javascript
function print(){
    console.log("hello world")
}
setTimeout(print,0)
console.log("play") // o/p will be "play" then "hello world"
```

# setInterval()

* setInterval() run the function repeatedly after the given interval of time.
```javascript
function print(){
    console.log("hello world")
}
setInterval(print,3000) // print "hello world" repeatedly every 3sec interval
```

# clearInterval()

* clearInterval() method clears a timer set with the setInterval() method.
```javascript
var play = setInterval(function(){
    console.log("Hello")
    }, 2000);
clearInterval(play); // It stop the setInterval 
```

# ParseInt()

* It converts non-integer number to a integer number. It always gives absolute number.
```javascript
console.log(parseInt("99")); // 99
console.log(parseInt("Welcome!")); // NaN
console.log(parseInt("99educative76")); // 99
console.log(parseInt("2019 4 29")); // 2019
console.log(parseInt("10.33")); // 10
```
# ParseFloat()

* It converts non-floating number to afloating number.
```javascript
console.log(parseFloat(3.14)); // 3.14
console.log(parseFloat('3.14')); // 3.14
console.log(parseFloat('  3.14  ')); //3.14
```

# JSON

* JSON stands for "Javascript Object Notation". It is just a data format.
* Object is the data that we use inside the system but outside it used as JSON value.

**JSON.stringfy()** - This method is used to convert object to json format for sending outide the system.
```javascript
let person = {
     name:"babul",                    
     age: 24, 
     hobby:"dance"
}

let value = JSON.stringify(person);
console.log(value); // '{"name":"babul","age":24,"hobby":"dance"}'
```
**JSON.parse()** - This method used to convert json format to object while receving data from outside.
```javascript
let value = '{"name":"babul","age":24,"hobby":"dance"}'
let person = JSON.parse(value)
console.log(person) // { name: "babul", age: 24, hobby: "dance" }
```

# Spread operator

```javascript
let value = ['a', 'b', 'c'];
let value2 = [...value, 'e', 'f'];
console.log(value2) //  ["a", "b", "c", "e", "f"]
```
```javascript
let value = ['a', 'b', 'c'];
let value2 = ['e', 'f', 'g'];
let value3 = [...value,...value2]
console.log(value3) //  ["a", "b", "c", "e", "f", "g"]
```

# Destructing

**Object destructing**
```javascript
let obj = {
    name : "babul",
    age : 24,
    hobby : {
        first : "dancing",
        second : "gym"
    }
}

let { name } = obj ;
let { hobby: {second}} = obj;
console.log (`${name} hobby is ${second}`) // babul hobby is gym
```

**Array destructing**
```javascript
let fruit = ["mango", "banana", "apple"];
let [a,b,c] = fruit             
console.log(a) // "mango"
console.log(b) // "banana"
console.log(c) // "apple"
```   

# Template Literal

```javascript
let name = "babul";
let fruit1 = "orange";
let fruit2 = "apple";
console.log(`Hey my name is ${name} and my favourite fruits are ${fruit1} and ${fruit2}`)

o/p - Hey my name is babul and my favourite fruits are orange and apple
```

