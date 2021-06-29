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


Sets

Sets are collections of values just like arrays, except they have two differences. First one is items in sets aren’t stored in any order. - random order. Second, all items must be unique, can’t appear twice in a set.

Tuples

Tuples allow you to store several values together in a single value.
They size are fixed.
Can’t change the type of items in tuple. 

var name = (first: “Minja”, last: “Zivanovic”)
name.0
name.first


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



Optionals


Swift is a very safe language, it works hard to ensure your code never fails. Most common ways that code fails is when it tries to use data that is bad or missing.
Swift has solution: Optionals. An optional value is one that might have a value or might not.

When we use -> String, it means “this will definitely return a string” which means this function cannot return no value. If we wanted to tell Swift that this function might return a value or it might not, we need to use this instead String? - question mark means “optional String”. 
In Swift no value has a special name: nil.

Swift wants your code to be safe, and trying to use a nil value is a bad idea. It might screw up your app logic, or it might make your user interface show the wrong thing. When you declare a value as optionals Swift will make sure you handle it safely. 

Swift has two solutions first solutions is called optional unwrapping, and it’s done inside a conditional statement using special syntax. it does two things at same time: check optional has a value and if it does unwraps it into a non-optional type then runs code block. 

When you work with these “might be there, might be not” value Swift force you to unwrap them before using them. That’s what if let syntax does, if the optional has a value then unwrap it and use it, otherwise don’t use it at all.


Force unwrapping optionals

Swift lets you override it’s safety by the exclamation mark character ( ! ). If you know that an optional has a value you can force unwrap it by placing this exclamation mark after it. but you have to be careful, if you try this  on a varible that does not have a value, your code will crash.


Implicitly unwrapped optionals

You can use this syntax, exclamation mark syntax to create implicitly unwrapped optionals.

Regular variable must contain a value.
Optional variable might contain a value or might not. It must be unwrapped before it is used.

An implicitly unwrapped optional might contain a value or might not, but it does not need to be unwrapped before it is used. Swift wont’t check for you so you need to be extra careful.

There are two times you ar goring to meet implicitly unwrapped optionals. The first is when you’re working with 🍏 API’s, these frequently return implicitly unwrapped optionals, because their code  pre-dates Swift, and that was not how things were done.

The second is when you’re working with user interface elements in UIKit. These need to be declared up front, but you can’t use them until they have been created by iOS and it likes to create user interface elements at the last possible moment to avoid any unnecessary work.


Optional chaining

Swift has two techniques to help make code less complicated working with optionals. First is called optional chaining which lets you run code only if your optional has a value.

Everything after question mark, which is the optional chaining, will be run if everything before the question mark has a value. Swift will check the code from left to right until finds nil, at which point it stops.


The nil coaleascing operator 

Double question mark is the nil coalescing operator ( ?? ). What it does is let you say use value A if you can, but if value A is nil then use value B. So if A is an optional and has a value it gets used If A is present and has no value B gets used, you will definitely have a value.


Enumerations

Called enum, are way to define your own kind of value. In some other programming languages they are simple little things, but Swift adds a huge amount of power to them.
Enum is useful inside switch / case blocks because Swift knows you might enum can have.


Enums with additional values

Enum can have values attached to them. 


Structs

Structs are complex data types, they are made up of multiple values. You then create instance of the struct and fill in its values. Then you can pass it around as a single value in your code. 
When you define struct, Swift makes memberwise initializer, that means you create struct passing initial values for its properties.

Once you created an instance of struct you can read its properties just by writing the name of the struct, a period, then the property you want read.



Classes

Class is another way of build complex data types called classes. They look similar to struct, but have a number of important differences:
Don’t have automatic memberwise initializer for classes, you need to write your own.
Can define class as being based off another class adding new thing 
If you copy an object, both copies point at the same data default



Initializing an object

In sturct Swift automatically produces a memberwise initializer for us that forced us to provide values for the properties. But that doesn’t happen with classes so Swift can’t sure they will be given values.

There are three solutions: make the values optional strings, give them default values, or write own initializers. 
The first option is clumsy because it introduces optionals all over our code where they don’t need to be. Th second option works, only if default values will be used. Third option is the right one, write our initializer.

To do this create a function inside the class called init() that takes the parameters we care about.

First you don’t write func before init() function.Second, because the parameter names being passed in are the same as the names of the properties we want to assign, you use self. to make your meaning clear.
When you write function inside the class, it’s called a method. In Swift you write func whether it’s a function or a method.
And Swift requires that all non-optional properties have a value by the end of the initiaizer, or by the time the initializer calls any other method, which ever comes first.


Class inheritance

The second difference between classes and structs are that classes can build on each other to produce greater things, known as class inheritance. This technique is used in Cocoa Touch, even in the most basic programs.


class Singer {
var name: String
var age: Int

init(name: String, age: Int) {
self.name = name
self.age = age 

}

func sing() {
print(“La la la la la”) 

    }
}

Now we can create an instance of that object calling initializer, then read out its properties and call its method:

vat taylor = Singer(name: “Taylor”, age: 25)
taylor.name
taylor.age
taylor.sing()

That is the basic class.
Now if we want to define CountrySinger class that has everything Singer class does.

class CountrySinger: Singer {

}

That colon means CountrySinger extends Singer, and we called subclass, and Singer we called parent class, or superclass.
If you want to have its own sing() method you need to override, that means, method that is implemented by parent class I want to change it for this subclass.
If you don’t use the override Swift will not change a method, and if you want to override and there wasn;t anything to override Swift will point out your error.

class CountySinger: Singer {

override func sing() {

print(“Trucks, girls, and liquor”)
 
     }
}


Now you want to make new class called HeavyMetal Singer, and store a new property called noiseLevel.
Swift wants all non optional properties to have a value
Singer class doesn’t have a noiseLevel property
You need to create a custom initilizer for HeavyMetalSinger that accepts a noise level
New initializer also needs to know the name and age of the heavy metal singer, so it can pass it onto the superclass Singer
Passing data to the superclass is done through a method call and you can’t make method calls in initializers until you have given all your properties values
So you need to set own property noiseLevel then pass on the other parameters for the superclass


class HeavyMetalSingerČ Singer {
var noiseLevel: Int 

init(name: String, Age: Int, noiseLevel: Int) {

self.noiseLevel = noiseLevel

super.init(name: name, age: age) 

}

override func sing() {
print(“Grrrrrrrr rarghhhh rargrrrrr rarrrrrrgh”)

   }

}

Values VS References 

When you copy a struct whole thing is duplicated, including all its values. This means that changing one copy of a struct doesn’t change the other copies, they are all individual. 
With classes each copy of an object points at the same original object, so if you change one, they all change. 
Swift calls struct value types because they just point at a value, and classes reference type, because objects are just shared references to the real value.

Value types:
String
Integer
Double
Boolean
Array
Enum
Dictionary
Set
Tuple
Struct

References types:

Classes
Closures 

The difference between value types and refereces types are imporatnt, and choice between struct and classes. 

If you want to have one shared state that gets passed around and modified in place, you are looking for classes. You can pass them into functions or store them in arrays, modify them in there and have that change reflected in the rest of your program.

If you want to avoid shared state where one copy can’t affect all the others you are looking for structs. You can pass them into functions, or store them in arrays, modify them in there, and they won’t change wherever else they are referenced.

To summarise this difference between structs and classes: classes offer more flexibility, where structs offer more safety. Basic rule always use structs until you have a reason to use classes.
Properties

Structs and classes can have theis own variables and constatnts and these are called properties.

These let you attach values to your types to represent them uniquely but because types can also have methods you can have behave according to their own data.

Methods are functions that are associated with a particular type, classes, structs and enums.

struct Person {
var clothes: String
var shoes: String

func describe() {
print(“I like wearing \(clothes) with \(shoes)”)

    }
}

let teylor = Person(clothes: “T-shirt”, shoes: “sneakers”) 
let other = Person(clothes: “short skirts”, shoes: “high heels”)

teylor. describe()
other.describe()


When we use property inside a method it will automatically use the value that belongs to the same object.

Properties are associate values with a particular class, structure or enumeration. 
Stored properties store constant and variable value as part of an instance, whereas computed properties calculate (rather than store) a value. 
Computed properties are provided by classes, structures, and enumerations. Stored properties are provided only by classes and structures.

Stored and computed properties are usually associated with instance of a particular type. However, properties can also be associated with the type itself. Such properties are known as type properties. 

In addition you can define property observers to monitor changes in a property’s value, witch you can respond to with custom actions. Property observers can be added to stored properties you define yourself, and also to properties that a subclass inherits from its superclass. 

Property observers

Swift let you add code to be run when a property is about to be changed or has been changed. This is frequently a good way to have a user interface update when a value change.

There a two kinds of observer: 

willSet

didSet

and they are called before or after a property is changed.

In willSet Swift provides your code with a special value called newValue that contains what the new property value is going to be.
In didSet you are given old value to represent the previous vale. 

struct person {
var clothes: String {

willSet {
updateUI(“I’m changing from \(clothes) to \(newValue)”) 

didSet {
updateUI(“I just changed from \(oldValue) to \(clothes)”) 

      }
   }
}

func updateUI(msg: String) {
print(msg)

var taylor = Person(clothes: “T-shirts”) 
taylor.clothes = “short skirts” 


Computed properties

Computed properties are common in Apple’s code by less common in our code. Many programmers prefer to use methods because their behavior is a clearer.


Static properties and methods

Swift lets you create properties and methods that belong to a type, rather than to instance of a type. This is helpful to organizing your data.
Swift calls these shared properties “static properties”, and you create one just by using the static keyword. Once that is done you access the property by using the full name of the type.

Basic static methods belong to the class rather than to instance of a class, you can’t use it to access any non-static properties from the class.


Access control

This is an important feature, it lets you specify what data inside structs and classes should be exposed to the outside world, and you get to choose three modifiers.

Public: everyone can read and write the property
Internal: only Swift code can read and write property
Private: only Swift code in the same file as the type can read and write the property

Most of the time you don’t need to specify access control, but sometimes you want to explicitly set a property to be private, because stops others from accessing it directly.


Polymorphism and type casting

Because classes can inherit each other it means one class is effectively a superset of another, class B has all the thing A has with a few extras. This in turn means that you can treat B as type B or as type A depending on your needs. 
Because any instance of class B is inherited from class A it can be treated just as either class A or class B. This is called “polymorhism”.

If you have class A, and data in the array are album, studio album, and live album, this is fine because Swift are all those data descended form the class we call the Album class, so they share the same basic behaviour.


Converting types with type casting

You will often find you have an object of a certain type, but really you know it’s a different type. Sadly, if Swift doesn’t know what you know, it won’t build your code. So there’s a solution, and it’s called type casting: converting an object of one type to another.
Type casting in Swift comes in three forms, but most of the time you’ll only meet two: as? and as!.
Known as optional downcasting (as?) and forces downcasting (as!). 
First one,  optional downcasting means “I think this conversation is true, but it might fail”.
Second one means “I know this conversion might be true, and I’m happy for my app to crash if I’m wrong”.
When I say “conversation” I don’t mean that the object literally transformed, instead it’s just converting how Swift treats the object, telling that an object it thought was type A is actually type E. 


Closures

Swift has another type of data that is used extensively in Swift, and it’s called a closure. 
Closure can be thought of as a variable that holds code, so where an nteger holds 0 a closure holds lines a lines of Swift code. It’s different to a function, because closures are a data type in their own right you can pass a closure as a oarameter or store it as a  property. Closures also capture the enviroment where are created, which means they take copy of the values that are inside them.


Project 1

This project produce an application that lets users scroll trought a list of images, then select one to view.

Behind the scenes an iOS app is actually a directory containing lots of files, all the media assets your app uses any visual layout files, plus a variety of other things such as metadata and security entitlements.
These app directories are called bundles. And they have the file extension .app. Because our media files are loose inside the folder, we can ask the system to tell us all the files that are in there pull out ones we want. You may have noticed that all the images start with the name “nssl”, so tas is simple, list all the files name in our app’s directory, and pull out the ones that start with “nssl”.
NSBundle nad NSFileManager are data types that can do some great work (NS is short for NeXTSTEP software that Apple bought in 1997., technology that still today lies at the heart of iOS). All UI (User Interface) NS data types are avalible on iOS.

UINavigatonController, means, UI - user interface component designed for iOS
Controller, part means it provides functionality.

Controllers are part of the holy trinity of software development: Model, View, Controller.
In a ideal world, every part of your app can be split info one of these three types.
Model: something that describes the data you are working with.
View: The user interface of your app
Controller: the code that sends model data to and from view.

Here are just some of the things we've covered, constants and variables, method overrides, table views and image views, app bundles, NSFileManager, typecasting, arrays, loops, optionals, view controllers, storyboards, outlets, Auto Layout, UIImage, image views.


Project 2

What is new:
Navigation Controller
UIButton
asset catalog

Making a game Guess the flag using UIKit, and learning about integers, buttons, collors and actions.
Guess the flag is the game that shows some random flags to user and ask them to choose wich one belongs to a particular country. 

Designing layout

In game we’re going to show user three flags, with the name of the country to guess shown in the navigation bar at the top.

Then we draw three UIButtons onto the canvas. Then resize them by jumping into size inspector. next step is to create Auto Layout rules.
Select flags from the project file and drag them into the Xcode window in your asset catalog.
Then you create outlet for each flag.




















