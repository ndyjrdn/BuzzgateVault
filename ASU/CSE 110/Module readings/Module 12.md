## 13.1 Procedural vs. object oriented programming

All objects have states or ==attributes== and behaviors or ==operations== 
***************
***************

Procedural programming is a package of responsibilities things is knows and things it does.  Variables and functions

object oriented programming aims to be more intuitive
Focus on identifying designing and creating objects.  This is done by creating classes

The objects know things and do things.  Variables and functions
***************
***************
## 13.2 classes and objects analogy

Classes define types of objects - it's attributes (the things it knows), and it's operations (the things it does)

## 13.3 object oriented programming
Creating an object is called instantiation.

## 13.4 instantiating objects
new classname argument

![[Pasted image 20251119120050.png]]
## 13.5 User defined functions
In an object oriented programming language like Java, we can also create our own classes. We do this in Java by writing a class definition. Here is a simple definition for a class named Bunny.  Note that a class defines a type of object, and objects are things; therefore our class names should generally be nouns or noun-like.
```java 
class Bunny {
	<classBody>
}
```

- three parts of basic class def:
	- keyword "class"
	- className
	- classBody
- *A class definition creates a new data type,* so by defining a class named Bunny we have created a Bunny data type. This means we can now declare variables of type Bunny.
## 13.6 useer defined classes and attributes
Class diagram:
![[Pasted image 20251119121154.png]]

attributes are accessed with .notation.  
myBunny.age.

The state of the object is contained in it attributes.  This is encapsulation

## 13.7 User defined classes and operations
updated class diagram
![[Pasted image 20251119121837.png]]
``` java 
class Bunny {
   int age;
   String name;

   void hop() {
       System.out.println(name + " hops around.");
   }

   void eat(String food) {
       System.out.println(name + " eats the " + food + ".");
   }

   void sleep() {
       System.out.println(name + " takes a nap.");
   }

}
// note the methods are NOT static
Bunny myBunny = new Bunny();

//access methods with dot notations myBunny.hop()

```

## 13.8 Objects: introduction
- In programming, an object is a grouping of data (variables) and operations that can be performed on that data (methods).
- Abstraction means having the user interact with an item at a high level - with low lever internals hidden **information hiding or encapsulation**
- abstract data type(ADT) is a data type whose creation and update are constrained to specific well-defined operations. A class can be used to implement an ADT.

## 13.9 using a class
- The class construct defines a new type that can group data and methods to form an object.
- A class' **public member methods** indicate all operations a class user can perform on the object.
- `Restaurant favLunchPlace = new Restaurant();` creates a Restaurant object named favLunchPlace.

## 13.10 defining a class
- private fields - variables that member methods can access but class users cannot
- 