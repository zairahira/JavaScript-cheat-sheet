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















