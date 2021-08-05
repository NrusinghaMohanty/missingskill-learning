
# Different index method of Array,Object and string

## Array

* JavaScript array is an object that represents a collection of similar type of elements.
* An array is a special type of variable, which can store multiple values using special syntax. Every value is associated with numeric index starting with 0.

**1. length** - To findout length of an array.
```javascript
var arr = [1,3,4,5,65]
console.log(arr.length) // 5
```

**2. push()** - It add new element in an array at the end.
```javascript
var arr = [1,3,4,5,65]
arr.push(36)
console.log(arr) // [1,3,4,5,65,36]
```

**3. pop()** - It remove last element in an array.
```javascript
var arr = [1,3,4,5,65]
arr.pop()
console.log(arr) // [1,3,4,5]
```

**4. unshift()** - It push new element in an array at the beginning.
```javascript
var arr = [1,3,4,5,65]
arr.unshift(36)
console.log(arr) // [36,1,3,4,5,65]
```

**5. shift()** - It remove first element in an array.
```javascript
var arr = [1,3,4,5,65]
arr.shift()
console.log(arr) // [3,4,5,65]
```

**6.  concat()** - It add/merge two array and create a new array.
```javascript
var arr = [1,3,4,5,65]
var arr2 = [8,6,9,4]
var arr3 = arr.concat(arr2)
console.log(arr3) // [1, 3, 4, 5, 65, 8, 6, 9, 4]
```

**7. forEach()** - It loop through each element of an array just like "for" loop.
```javascript
var arr = [1,3,4,5,65]
arr.forEach(function(element){
console.log(element);
}) // 1 3 4 5 65
```

**8. map()** - It creates a new array with the results of calling a function for every array element.
```javascript
var arr = [1,3,4,5,65]
var arr2 = arr.map(function(element){
 return element+1
}) 
console.log(arr2) // [2, 4, 5, 6, 66]
```

**9. filter** - It creates a new array with the element of calling array that passed the condition.
```javascript
var arr = [1,3,4,5,65,true]
var arr2=arr.filter(function(element) {
 return element === true
})
console.log(arr2) // [true]
```

**10. indexOf** - To know the index number of a given element in an array.
```javascript
var arr = [1,3,4,5,65]
var value = arr.indexOf(4)
console.log(value) // 2
```

**11. includes()** - It checks for the presence of a specific element in an array and gives boolean value according to that.
```javascript
var arr = [1, 3, 5, 2, 4];
var check = arr.includes(2);
var check2 = arr.includes(10)
console.log(check); // true
console.log(check2); // false
```

**12. join()** - It return a new string by concatenating all the elements of the array.
```javascript
var fruits = ["banana", "mango" , "apple" , "orange"]
var value = fruits.join(",")
var value2 = fruits.join("")
console.log(value) // "banana,mango,apple,orange"
console.log(value2) // "bananamangoappleorange"
```

**13. splice** - It takes two parameter that is index and a number. It remove given number of element from the array starting from given index number. 
```javascript
var arr = [1, 3, 5, 2, 4, 7];
arr.splice(2,3)
console.log (arr) // [1,3,7]

//splice remove 3 element from the 2nd index number
```

**14. slice()** - It takes two parameter that is starting index and ending index and create a new array from the element present at giveen starting index to the ending index but element present at ending index excluded.
```javascript
const numbers=[1,2,3,45,5];
const arr= numbers.slice(1,4);
console.log(arr) // [2,3,45]
```

**15. Array.isArray()** - To check the value is array or not. It gives a boolean value.
```javascript
var arr = [1, 3, 5, 2, 4, 7];
var arr2 = "Hello";
console.log(Array.isArray(arr)) // true
console.log(Array.isArray(arr2)) // false
```

# Object

**1. Object.keys()** - It convert the keys of object to an array.
```javascript
var obj = { "name":"babul","age":23,"hobby":"dance" }
var arr = Object.keys(obj)
console.log(arr) // ["name", "age", "hobby"]
```

**2. Object.assign()** - this method used to copy or merge objects.
```javascript
var fruit = { name: 'Mango', price: 200 };
var cloned_fruit = Object.assign({}, fruit);
console.log(cloned_fruit);  // { name: "Mango", price: 200 }
var Mango = Object.assign({weight: 500}, fruit);
console.log (Mango); // { weight: 500, name: "Mango", price: 200 }
```

**3. Object.freez()** - this methos used to freez an object. Freezing object doesn't allow any new properties to add or remove any xisting proprties.
```javascript
const obj1 = { property1: 'initial_data'};
        const obj2 = Object.freeze(obj1);
        obj2.property1 = 'new_data';
        console.log(obj2.property1); // "initial data"
 ```

**4. Object.toString()** - It converts object to string.


# String

**1. toUpperCase()** - It converts all the character in a string to uppercase(capital).
```javascript
var name = "RaHUl MoHaNty"
console.log(name.toUpperCase()) // "RAHUL MOHANTY"
```

**2. toLowercase()** - It converts all the character in a string to lowercase(small).
```javascript
var name = "RaHUl MoHaNty"
console.log(name.toLowerCase()) // "rahul mohanty"
```

**3. replace()** - It takes two parameter. It searches the first occurence of first paramter and replace with the second paramter in a string.
```javascript
var name = "Rahul Mohanty"
var name2 = name.replace("h","s")
console.log(name2) // "Rasul Mohanty"
```

**4. replaceAll()** - It takes two parameter. It searches for all occurences of first paramter and replace with second paramter in a string.
```javascript
var name = "Rahul Mohanty"
var name2 = name.replace("h","s")
console.log(name2) // "Rasul Mosanty"
```

**5. trim()** - It removes all the whitespace from beginning and end of the string.
```javascript
var name = "Rahul Mohanty     "
console.log(name.trim()) // "Rahul Mohanty"
```
**6. split()** - It converts a string into an array.
```javascript
var fruit = "Mango"
console.log(fruit.split("")) // ["M", "a", "n", "g", "o"]
```
