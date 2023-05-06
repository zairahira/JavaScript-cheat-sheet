# JS-cheat-sheet
A list of basic JS commands and concepts



## Comments

    // inline comment
    
    /*
    multi line comment
    */


## Printing to console

    console.log("Hello World");

## Data types

    undefined, null, boolean, string, symbol, number, object

Where,
symbol: immutable value
object: stores key value pair.

## Variable naming convention

    camelCase

## Declaring and initializing variables

    var a_variable;
    
    var myName = "Hero" // global
    console.log(myName)

    myName = 8

    myName++
    myName--

    let ourName = "freeCodeCamp" // let only within the scope
    
    const pi = 3.14 // const never changes
    
    console.log(pi)
    
    var c = ourName + myName //concatenate strings
    console.log(c)

## Compound assignment

    var a = a + 10;
    //same as 
    a+=10;
    a-=10;
    a*=10;
    a/=10;


## Declaring string variables

    var firstName = "Stephen"
    var lastName = "Hawkings"

## Escaping characters in strings

    var quoteWithinQuote = "A wiseman said, \"save your time\"";

string can also be surrounded by single quotes and back-ticks and then you don't need escape characters. with escape characters you can enclose both- single and double quotes.



Some more escape characters:

     
    \n //newline
    \t // tab space
    \backspace
    \f //form feed


## Join strings

    var ourName2 = "freeCodeCamp" ;
    var ourStr = "Hello, our name is" + ourName + "how are you?";

## Find length of a string 

    the_len = ourName.length;

## Access string characters indivudually

    access = ourName[0]; // returns f

> Strings are immutable means the individual letters can't be changed

    // throws error:
    var myString = "Jello world";
    myString[0] = "H"
    console.log(myString);

## Find the last caracter in a string:

    var lastCharacter = myString[myString.length - 1];

 

## functions madlibs example

```
function madlibs() {
  // Define an object to hold the words for the story
  const words = {
    adjective: prompt('Enter an adjective:'),
    noun: prompt('Enter a noun:'),
    verb: prompt('Enter a verb:'),
    adverb: prompt('Enter an adverb:')
  };
  
  // Construct the story using the input words
  const story = `The ${words.adjective} ${words.noun} ${words.verb} ${words.adverb}.`;
  
  // Display the story to the user
  alert(story);
}

// Example usage
madlibs();


```

## Arrays

    var ourArray = ["John", 23]; // can be a mix of string and numbers
    
    var myArray = [];

## Nested arrays or multidimensional array

    var ourArray = [["the universe"], 42];

## Accessing multidimensional array items

    console.log(ourArray[0])

## Modify array data

    myArray[0] = 45;

## Access multi dimensional array

    var myArray = [[1,2,3], [3,4,5], [5,6,7], [[10,11,12], 13, 14]];
    console.log(myArray[3][0][0]); // prints 10


## array push() function

    ourArray.push(["happy", "cat"]); // adds at the end of the array

## array pop()

    var ourArray = [1,2,3];
    var removedFromOurArray = ourArray.pop() // removes the last element

## array shift()

    var removedFromOurArray =  myArray.shift();// removes the first element

## array unshift()

    ourArray.unshift("Happy"); // adds element to beginning of the array

## nested arrays shopping list

    var myList = [["cereal", 3], ["juice", 2], ["eggs",12]];

## functions

    function ourReusableFunction(){
    	console.log("heyy");
    }
    
    ourReusableFunction(); //function call

## passing arguments to function

    function funcWithArcs(a, b) {
    	console.log(a - b);
    
    }
    
    funcWithArcs(10, 5);

## Global scope

    //global variable
    
    var myGlobal = 10;
    
    function fun1(){
    
    // myGlobal accessable
    
    }
    
    
    function fun2(){
    
    // myGlobal accessable
    	
    }

## local variable takes precedence as compared to global variable

    var outerWear = "T-Shirt" ;
    
    function myOutfit() {
    
    var outerWear = " sweater" ;
    return outerWear; // returns sweater
    
    }

## undefined values in functions

undefined when you dont specify a return value

## return values in function

     var changed = 0;
    
    function change(num) {
    return (num + 5) / 3;
    }
    
    changed = change(l0);

## queue LIFO

    function nextInLine(arr, item){
    
    arr.push (item) ;
    return arr.shift();
    }
    
    var testArr = [1,2,3,4,5];
    
    console.log("Before: " + JSON.stringify(testArr)) 
    console.log(nextInLine(testArr, 6))
    console. log ("After: " + JSON.stringify(testArr));
    
    // output:
    Before: [1,2,3,4,5]
    1
    After: [2,3,4,5,6]




## comparison with the equality operator

    function testEquaI(val) {
    if (val == 12) { // single = means assignment
    
    return "Equal" ;
    
    }
    
    return "Not Equal";

Notes:

In JavaScript, the = symbol is the assignment operator and is used to assign a value to a variable. For example, x = 5 assigns the value 5 to the variable x.

The == operator is used for equality comparison, which means it compares two values for equality, and returns a boolean true or false result. For example, 5 == "5" would return true because they have the same value, even though they have different types (5 is a number and "5" is a string).

It's important to note that the == operator performs type coercion, which means that it will attempt to convert the types of the values being compared if they are not already the same. This can sometimes lead to unexpected results. For example, 0 == false would return true, because false is coerced into the number 0 for the comparison.

To avoid the potential issues with type coercion, it's often recommended to use the === operator for strict equality comparison, which checks that the values being compared are of the same type as well as having the same value. For example, 5 === "5" would return false, because they are not of the same type.

## comparison with the strict equality operator


To avoid the potential issues with type coercion, it's often recommended to use the === operator for strict equality comparison, which checks that the values being compared are of the same type as well as having the same value. For example, 5 === "5" would return false, because they are not of the same type.



## comparison with the inequality operator

    if (val != 99) 

## comparison with the strict inequality operator

    if (val !== 77)

## and comparison

    if (val <=50 && val >=25){ // both need to be true
    	// do somethins
    }

## else statements


	if (true) {

	}

	else{

	}


## else if statements

    if() {
    
    }
    
    else if(){
    
    }
    
    else{
    
    }

## chaining if/else statements

    if(){
    // ... code body here
    }
    
    else if(){
    // ... code body here
    
    }
    
    else if(){
    // ... code body here
    
    }
    
    else if(){
    // ... code body here
    
    }
    
    else {
    // ... code body here
    
    }


## logical order

the sequence of execution is top down

## case statements

    switch (expression) {
      case value1:
        // code to be executed when expression matches value1
        break;
      case value2:
        // code to be executed when expression matches value2
        break;
      case value3:
        // code to be executed when expression matches value3
        break;
      default:
        // code to be executed if none of the cases match expression
    }

## multiple identical options in switch

    let num = 2;
    
    switch (num) {
      case 1:
      case 2:
      case 3:
        console.log("The number is between 1 and 3");
        break;
      case 4:
      case 5:
      case 6:
        console.log("The number is between 4 and 6");
        break;
      default:
        console.log("The number is not between 1 and 6");
    }


## returning booleans

    return a < b;

## returning early patterns in functions

Returning early patterns in functions is a technique in JavaScript where you can improve the readability and maintainability of your code by returning early from a function if certain conditions are met. Here are a few common patterns:



    function divide(num1, num2) {
      if (num2 === 0) {
        return 'Cannot divide by zero';
      }
      
      return num1 / num2;
    }

## build objects

    let myObject = {
      key1: value1,
      key2: value2,
      key3: value3,
      // ...
    };

    var theValue = myObject.key1; // would contain value1

## accessing object properties with variables

In JavaScript, you can access object properties using variables with either dot notation or bracket notation.

Using dot notation:
If you know the name of the property at the time of writing your code, you can use dot notation to access the object property. For example:

    let myObject = {
      name: "John",
      age: 30,
      city: "New York"
    };
    
    let propertyName = "name";
    console.log(myObject.name); // Outputs "John"
    console.log(myObject[propertyName]); // Outputs "John"

In this example, we use dot notation to access the name property of myObject. We also assign the string "name" to the propertyName variable, and then use bracket notation with myObject and propertyName enclosed in square brackets to access the name property dynamically.

Using bracket notation:
If you do not know the name of the property at the time of writing your code, or if the property name is stored in a variable, you can use bracket notation to access the object property. For example:

    let myObject = {
      name: "John",
      age: 30,
      city: "New York"
    };

    let propertyName = "name";
    console.log(myObject[propertyName]); // Outputs "John"
    
    let propertyName = "name";
    console.log(myObject[propertyName]); // Outputs "John"


In this example, we use bracket notation with myObject and propertyName enclosed in square brackets to access the name property dynamically.

It is important to note that if you use bracket notation with an invalid key or a non-existent property, it may result in an error. Therefore, you should always check if the property exists in the object before accessing it using a variable.

## add a new property to objects

    let myObject = {
      name: "John",
      age: 30,
      city: "New York"
    };
    
    myObject.parks = "many"; // would add another property

## delete property from objects

    delete myObject.parks;  

## testing objects for properties

    if(myObj.hasOwnProperty(checkProp));


## Manipulating complex objects and accessing nested objects

    const person = {
      name: 'John Doe',
      age: 30,
      address: {
        street: '123 Main St',
        city: 'Anytown',
        state: 'CA',
        zipCode: '12345',
        country: 'USA'
      },
      hobbies: ['reading', 'painting', 'hiking']
    };

In this example, the person object contains several properties, including an address object and an array of hobbies. The address object is a nested object, containing its own set of properties such as street, city, state, zipCode, and country. This type of nesting is commonly used to organize and represent complex data structures in a clear and organized way.
 
## While loops

    let count = 1;
    
    while (count <= 5) {
      console.log(count);
      count++;
    }

## For loop

    for (let i = 1; i <= 5; i++) {
      console.log(i);
    }


## backward for loop

    for (let i = 5; i >= 1; i--) {
      console.log(i);
    }


## do while

    let i = 1;
    
    do {
      console.log(i);
      i++;
    } while (i <= 5);


## Math functions

    Math.random();
    Math.floor(Math.random() * 20); // rounded whole numbers between 1 and 20





## Convert string to int using parseInt

    function convertToInteger(str) {
        return parseInt(str, 2); // base 2 binary number
        
    }
    
    
    console.log(convertToInteger("10011"));

## Ternary operator

    condition ? expression1 : expression2

In this syntax, condition is the expression that evaluates to a boolean value (either true or false), and expression1 and expression2 are two expressions that can be of any type.

The ternary operator works by first evaluating the condition. If the condition is true, the ternary operator returns the value of expression1. If the condition is false, the ternary operator returns the value of expression2.

Here's an example that uses the ternary operator to check if a number is even or odd:


```
const number = 5;
const isEven = number % 2 === 0 ? true : false;

console.log(isEven); // Output: false


```

## nesting ternary operators

```
const score = 85;

const grade = score >= 90 ? "A" :
              score >= 80 ? "B" :
              score >= 70 ? "C" :
              score >= 60 ? "D" : "F";

console.log(`The student's grade is ${grade}.`);


```

In this example, we first declare a constant score and set it to 85. We then use nested ternary operators to determine the grade of the student based on their score.

The first ternary operator checks if the score is greater than or equal to 90. If it is, the operator returns the string "A". If it is not, the second ternary operator is evaluated.

The second ternary operator checks if the score is greater than or equal to 80. If it is, the operator returns the string "B". If it is not, the third ternary operator is evaluated.

The third ternary operator checks if the score is greater than or equal to 70. If it is, the operator returns the string "C". If it is not, the fourth ternary operator is evaluated.

The fourth ternary operator checks if the score is greater than or equal to 60. If it is, the operator returns the string "D". If it is not, the operator returns the string "F".

Finally, we assign the result of the nested ternary operators to the constant grade and log it to the console.

The output of this code would be:

```
The student's grade is B.
```

## Difference between var and let

`let` does not let you declare a variable twice

This code returns an error:

```

let catname = "arearre";
let catname = "arewr"

```

In JavaScript, var and let are both used to declare variables, but they have some important differences in terms of their scope and behavior.

Here are some of the key differences between var and let:

**Scoping:** Variables declared with var are function-scoped, which means that they are accessible throughout the entire function in which they are declared, including any nested functions. Variables declared with let, on the other hand, are block-scoped, which means that they are only accessible within the block in which they are declared (e.g., within a loop or an if statement).

**Hoisting**: Variables declared with var are hoisted to the top of their scope, which means that they can be accessed before they are declared (although their value will be undefined until they are assigned a value). Variables declared with let, on the other hand, are not hoisted, and cannot be accessed before they are declared.

**Reassignment**: Variables declared with var can be reassigned within their scope, while variables declared with let can be reassigned as well, but they can only be declared once within their scope.

Here's an example that demonstrates some of these differences:

```
function example() {
  var x = 1;
  let y = 2;

  if (true) {
    var x = 3;
    let y = 4;
    console.log(x, y); // Output: 3, 4
  }

  console.log(x, y); // Output: 3, 2
}

example();


```
In this example, we declare two variables, x and y, using var and let, respectively. We then use an if statement to declare a new variable x and y within the block. Note that the var x declaration within the block is actually reassigning the original x variable, which is why the value of x is 3 both within and outside of the block. The let y declaration within the block, on the other hand, creates a new y variable that is only accessible within the block.

Output:

```
3 4
3 2

```




## `use strict` to catch coding errors

Used to catch common errors and coding errors
usually used at the top of the code
use all caps, variable naming convention.
syntax:

    "use strict";

## const

const has all the features of let but also read only.
cant be reassigned.


const is a keyword in JavaScript used to declare a variable that is read-only and cannot be reassigned a new value after it has been initialized.

Here's an example:

```
const PI = 3.14;
```

In this example, we use const to declare a variable PI and assign it the value 3.14. Once the PI variable has been initialized, it cannot be reassigned a new value. For example, the following code would result in a TypeError:


```
const PI = 3.14;
PI = 4.0; // TypeError: Assignment to constant variable.
```

One important thing to note is that const only creates read-only bindings for the variable itself. It does not make the value immutable. If the value is an object or an array, its properties or elements can still be modified. For example:

```
const arr = [1, 2, 3];
arr.push(4); // This is allowed
console.log(arr); // Output: [1, 2, 3, 4]
```

In this example, the arr variable is declared using const, but its elements can still be modified using the push method. However, reassigning arr to a new array would still result in a TypeError, since the variable itself cannot be reassigned.


## mutate an array with const

You can still mutate an array and an object even if it is declared using `const`.


```
const arr = [1, 2, 3];
arr[0]=77; // This is allowed
console.log(arr); // Output: [ 77, 2, 3 ]

```

## prevent object mutation

object or array declared with const can still be mutated.
so,

`object.freeze` can prevent data mutation

In JavaScript, the Object.freeze() method can be used to prevent the mutation of an object. When an object is frozen, its properties cannot be added, deleted, or modified.



example:

```
const person = {
    name: "John",
    age: 30
  };
  
 Object.freeze(person);
  
  person.age = 31;
  console.log(person.age); // Output: 30
  
```

In this example, we create an object person with two properties, name and age. We then use Object.freeze() to freeze the object, making it immutable. When we attempt to change the value of person.age, the assignment has no effect and the value of person.age remains at 30.

Note that Object.freeze() only freezes the first level of an object's properties. If the object contains nested objects or arrays, those nested objects and arrays are not frozen and their properties can still be modified.

Here's an example to illustrate this:


```
const person = {
  name: "John",
  address: {
    city: "New York",
    state: "NY"
  }
};

Object.freeze(person);

person.address.city = "Boston";
console.log(person.address.city); // Output: "Boston"

```


## arrow functions to write concise anonymous functions

This is an anonymous function as it isn't named

```

var magic = function() {

return new Date();

}

```

we can shorten this code like this using the arrow func:

general syntax:

```
(parameters) => { statement }


```


```
const  magic = () => new Date();
```

another ex

```
const add = (x, y) => {
  return x + y;
};

console.log(add(2, 3)); // Output: 5


```

## higher order arrow funcs

we can use default parameters
kicks in when the argument is not defined.

// need more deets

## rest operator `...`

takes a variable number of arguments

the ... converts everthing passed into an array called args

```

const sum = (...numbers) => {
  return numbers.reduce((total, num) => {
    return total + num;
  }, 0);
}

console.log(sum(1, 2, 3, 4, 5)); // Output: 15
console.log(sum(10, 20, 30)); // Output: 60

```

In this example, the sum function takes an arbitrary number of arguments using the rest operator ...numbers. This creates an array called numbers that contains all of the arguments passed to the function.

Inside the function, we use the reduce() method to add up all of the numbers in the numbers array and return the total. The reduce() method takes a callback function that is called for each element in the array and accumulates the total value.

The `, 0`  initializes the total parameter to 0 for the first call to the callback function. This means that the first value added to total will be the first element in the array. If the initial value is not specified, the first call to the callback function will use the first two elements of the array as the initial values.


Finally, we call the sum function with different numbers of arguments and print the results to the console.

Using the rest operator in this way allows us to write a more flexible and reusable function that can handle an arbitrary number of arguments without having to specify them all individually.


## spread operator to evaluate arrays

spreads out an array
here's an example of the spread operator (...) in JavaScript:

```
const numbers = [1, 2, 3, 4, 5];
const newArray = [...numbers, 6, 7, 8];

console.log(newArray); // Output: [1, 2, 3, 4, 5, 6, 7, 8]

```

In this example, we have an array of numbers called numbers. We use the spread operator ... to "spread" the elements of the numbers array into a new array called newArray. We then add three additional numbers (6, 7, and 8) to the end of the newArray.

The result is a new array that contains all of the elements of the numbers array followed by the three additional numbers.

The spread operator is useful for concatenating arrays, creating new arrays that are subsets of existing arrays, and passing arrays as arguments to functions. It can also be used with objects to merge object properties.


## Destructuring assignments

```
const AVG_TEMPERATURES = {
    today: 77.5,
    tomorrow: 79

    
};


function getTempOfTmrw(avgTemperatures) {

    "use strict";

// means assign value of `tomorrow` from object avgTemperatures to `tempOfTomorrow`
const { tomorrow : tempOfTomorrow }= avgTemperatures;
return tempOfTomorrow;
}

console.log(getTempOfTmrw(AVG_TEMPERATURES));
```


## template literals

make stringsmore versatilr
uses backticks
you can make multiline strings with it

you can add single/ double quotation marks without escaping

you can add variables values wihtin too

```
const person = {
    name: "Zodiac Hasbro",
    age: 56
    
}

// Template literal with multi-line and string interpolation
const greeting = `Hello, my name is ${person.name} !
I am ${person.age} years old.`

console.log( greeting) ;
```

output also shows new line


## object can contain a function


```
const bicycle = {
    gear: 2,

    setGear(newGear) {
    "use strict";
    
    this.gear = newGear;
    }
};

bicycle.setGear(3) ;
console.log (bicycle.gear) ;

```

## class syntax to define a constructor function

```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

const person1 = new Person('Alice', 25);
const person2 = new Person('Bob', 30);

person1.sayHello(); // Output: "Hello, my name is Alice and I am 25 years old."
person2.sayHello(); // Output: "Hello, my name is Bob and I am 30 years old."


```

In this example, we define a Person class with a constructor function that takes two parameters: name and age. Inside the constructor function, we use the this keyword to set the name and age properties of the newly created Person object.

We also define a sayHello method on the Person class that logs a message to the console using the name and age properties.

Finally, we create two Person objects using the new keyword and the Person constructor function, and call the sayHello method on each object to output a message to the console.

Using class syntax in this way allows us to create reusable object blueprints with properties and methods that can be used to create multiple instances of the object with different values.

## getter and setter

```

class Rectangle {
  constructor(width, height) {
    this._width = width;
    this._height = height;
  }

  get width() {
    return this._width;
  }

  set width(newWidth) {
    if (newWidth > 0) {
      this._width = newWidth;
    }
  }

  get height() {
    return this._height;
  }

  set height(newHeight) {
    if (newHeight > 0) {
      this._height = newHeight;
    }
  }

  get area() {
    return this._width * this._height;
  }
}

const rectangle1 = new Rectangle(10, 20);

console.log(rectangle1.width); // Output: 10
console.log(rectangle1.height); // Output: 20
console.log(rectangle1.area); // Output: 200

rectangle1.width = 15;
rectangle1.height = 30;

console.log(rectangle1.width); // Output: 15
console.log(rectangle1.height); // Output: 30
console.log(rectangle1.area); // Output: 450


```






















