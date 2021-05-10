# 100DaysOfSwift
Paul Hudson's 100 Days Of Swift challenge 


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


Conditional statements

Sometimes you want code to execute only if certain condition is true, and in Swift that is represented primarily bu the if and else statements. 
First step is give Swift a condition to check, second a block of code to execute if condition is true.
Also you can write else and provide a block of code to execute if condition is false, or even else if  and have more conditions.

Also you can write else and provide a block of code to execute if condition is false, or even else if  and have more conditions.


Evaluation multiple conditions

Swift can evaluate as many conditions as you want, but they all need to be true in order to execute the block of code. 
To check multiple conditions use the && operator, it means “and”.


Looking for the opposite of truth

Sometimes is important to check is condition false ( not true ), you can do this with the ( ! ) operator.


Loops 

Simple programming constructs that repeat a block of code for as long as condition is true.
Close range operator is three periods in a row ( … )
Half open range operator looks like ( ..< ) and counts from one number up to and excluding another, for example 1..<5 will count 1, 2, 3, and 4.


Looping over arrays

Swift can loop over all the elements in an array because Swift knows what kind of data array holds, it will go through every element in array assign it to a constant you name and then run a block of code.
Also you can use for i in loop construct to loop through arrays, because you can use that constant to index into an array. 


Inner loops

You can put loops inside the loops.
Even loop inside the loops inside the loops.


While loops

While loops are third kind of loop, which repeat a block of code until you tell it to stop.
Keyword is called break, it’s used to exit a while or for loop at the point you decide. Without the keyword break, statement the loop is an infinite loop.

Counterpart to break is called continue. Breaking out of a loop stops execution immediately and continues directly after the loop, counting a loop only exits the current iteration of the loop, it will be jump back to the top of the loop and pick up from there.


Switch case

Another type of flow control called switch / case, it’s advanced for if statement, because you can have lots of matches and Swift will execute the right one.


Functions

Functions let you define reusable pieces of code that perform specific functionality.


Return values


Functions can return a value by writing -> then a data type. Swift will ensure that your function will return a value no matter what, and you make a promise about what your code does.
















