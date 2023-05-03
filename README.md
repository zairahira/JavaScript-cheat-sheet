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
























