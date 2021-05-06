# 100DaysOfSwift
Paul Hudson's 100 Days Of Swift challenge 

Day 1.

Variables and Constants

Program needs to store data. In Swift there are two ways to do it, variables and constants.
Variables is a data store that can have its value changed whenever you want. Constants is a data store that you set once and can never change. 
Variable using var keyword var.
Constant use the let keyword.
Variable and constant names must be unique in code.


Types of Data

There are lots of kinds of data and Swift handles them individually. 
Strings, literally a string of characters, can be long or empty.
Another important data type are called Int, short for integer. Integers are round numbers. 


Float and Double

Swift have two more data types to store data called Float and Double. This is a Swift way to store data with fractional numbers: 3, 30, 300.
Official Apple recommendation is always to use Double because it has highest accuracy. 


Boolean

Swift has a built in data type that can store value true or false, called Bool, short for Boolean.


Using type annotations wisely

There is two ways to tell Swift what type of data a variable holds, assign a value when you the create the variable, or use a type annotation. If you have a choice, the first is always preferable because it’s clearer.
The technique is called type inference, because Swift can infer what data type should be used for a variable by looking at the type of data you want to put in there.


Operators

Operators are symbols form math; +, -, =, *, /, they all exist in Swift.

+= is an operator that means add then assign to.


Copmarison operators

Swift has a set of operators that perform comparisons on value.

(>) - greater
(>=) - greater then or equal
(<) - less then 
(=) - equal
(==) - is equal to
(!) - not, that mean the opposite of what it did


String interpolation

String interoplation is a very simple thing, combining variables and constants inside a string. 

Day 2. 

Arrays

Arrays let you group lots of values together into a single collection, then access those values by their positions in the collection. 
Swift uses type inference to figure out what type of data your array holds.
When it comes to reading items out an array, there’s a catch, Swift starts counting at 0. This means the first item is 0, the second items is 1, the third is 2 and so on. 
Item’s position in an array is called its index, and you can read any item from the array just by providing its index. 


Creating arrays

Write var sons: [String], that tells Swift the songs variable will hold an array of string, buy doesn’t actually create that array. It doesn’t allocate RAM. It just says that at some point there will be array an it will hold strings.

var songs = [String]()

The () tells Swift I want to create the array which is then assigned to songs using type inference.


Array operstors

You can use limited set of operators on arrays:

and += 


Dictionaries

Dictionaries are another type of collection, but different. When you make dictionary you write it’s key, then a colon, then its value.
You can read any value from the dictionary just by knowing it’s key.
As arrays, you can store a wide variety of values inside dictionaries, although the keys are most commonly strings.








