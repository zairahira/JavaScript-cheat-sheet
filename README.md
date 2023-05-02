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












