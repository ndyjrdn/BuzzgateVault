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

## 13.11 mutators, accessors and private helpers
- A classes public methods are either mutators are accessors:
	- A ==mutator== may modify a classes fields (setter)
	- An ==accessor== accesses but does not change the fields(getter)
	
### Example
```java
public class Restaurant {                          
   private String name;
   private int rating;

   public void setName(String restaurantName) {  // Mutator
      name = restaurantName;
   }

   public void setRating(int userRating) {       // Mutator
      rating = userRating;
   }

   public String getName() {  // Accessor
      return name;
   }

   public int getRating() {  // Accessor
      return rating;
   }

   public void print() {      // Accessor
      System.out.println(name + " -- " + rating);
   }
}

public class MyRestaurant {
  public static void main(String[] args) {
     Restaurant myPlace = new Restaurant();
     myPlace.setName("Maria's Diner");
     myPlace.setRating(5);
     System.out.print(myPlace.getName() + " is rated ");
     System.out.println(myPlace.getRating());
  }
}
```
- private helper methods help public methods carry out tasks

## 13.12 Initialization and constructors
- Field initialization
- In a class a programmer can initialize fields in the field declaration.  Any object created of that class type will initially have those values
- Example
- 
```java
  public class Restaurant {   
  ###########################
  // The next 2 lines are init fields  
  ##############################                     
   private String name = "NoName";   
   private int rating = -1;
   public void setName(String restaurantName) {  
      name = restaurantName;
   }

   public void setRating(int userRating) {
      rating = userRating;
   }

   public void print() {  
      System.out.println(name + " -- " + rating);
   }
}

public class RestaurantFavorites {
   public static void main(String[] args) {
      Restaurant favLunchPlace = new Restaurant(); // Initializes fields with values in class definition

      favLunchPlace.print();

      favLunchPlace.setName("Central Deli");
      favLunchPlace.setRating(4);
      
      favLunchPlace.print();
   }
}
```

- Constructors
- ==Java provides a special class member method, known as a constructor, that is called when an object of that class type is created, and which can be used to initialize all fields. The constructor has the same name as the class. The constructor method has no return type, not even void. Ex: `public Restaurant() {...}` defines a constructor for the Restaurant class.==
- A programmer specifies the constructor that should be called when creating an object. Ex: `Restaurant favLunchPlace = new Restaurant();` creates a new Restaurant object and calls the constructor Restaurant().
- If a class does not have a programmer-defined constructor, then the Java compiler _implicitly_ defines a default constructor with no arguments. The Java compiler also initializes all fields to their default values.
```java
public class Restaurant {
   private String name;
   private int rating;

   public Restaurant() {  // Constructor with no arguments      
   name = "NoName";    // Default name: NoName indicates name was not set      
   rating = -1;        // Default rating: -1 indicates rating was not set   }
   public void setName(String restaurantName) {
      name = restaurantName;
   }

   public void setRating(int userRating) {
      rating = userRating;
   }

   public void print() {
      System.out.println(name + " -- " + rating);
   }
}

public class RestaurantFavorites {
   public static void main(String[] args) {
      Restaurant favLunchPlace = new Restaurant(); // Calls the constructor

      favLunchPlace.print();

      favLunchPlace.setName("Central Deli");
      favLunchPlace.setRating(4);
      favLunchPlace.print();
   }
}
```

## 13.4 defining main() in programmer defined class
==main() is a static method that is independent of class objects. main() can access other static methods and static fields of the class, but cannot directly access non-static methods or fields==
```java
public class BasicCar {

   // Total miles driven by the car
   private int milesDriven;
    
   // Constructor assigns initial values to instance variables
   public BasicCar() {
      milesDriven = 0;   
   }

   // Drive the requested miles
   public void drive(int tripMiles) {
      milesDriven = milesDriven + tripMiles;
   }

   // Return total number of miles driven
   public int checkOdometer() {
      return milesDriven;
   }

   // Main() creates objects of type BasicCar and 
   // calls methods to operate on the objects
   public static void main(String [] args) {BasicCar redCorvette = new BasicCar();      
   BasicCar fordMustang = new BasicCar();
    redCorvette.drive(100);     
    fordMustang.drive(75);      
    fordMustang.drive(300);      
    fordMustang.drive(50);   }
}
```
![[Pasted image 20251120130232.png]]
## 13.15 Unit Testing (classes)
- A testbench is a program whose job is to thoroughly test another program (or portion) via a series of input/output checks known as test cases. ==Unit testing means to create and run a testbench for a specific item (or "unit") like a method or a class.==
- 🎏**Features of a good testbench include:**

- Automatic checks. Ex: Values are compared, as in `testData.GetNum1() != 100`. For conciseness, only fails are printed.
- Independent test cases. Ex: The test case for GetAverage() assigns new values, vs. relying on earlier values.
- 100% code coverage: Every line of code is executed. A good testbench would have more test cases than below.
- Includes not just typical values but also border cases: Unusual or extreme test case values like 0, negative numbers, or large numbers.

### Regression testing
Regression testing means to retest an item like a class anytime that item is changed; if previously-passed test cases fail, the item has "regressed"
A testbench should be maintained along with the item, to always be usable for regression testing.

Testbenches may be complex, with thousands of test cases. Various tools support testing, and companies employ _test engineers_ who only test other programmers' items. ==A large percent, like 50% or more, of commercial software development time may go into testing.==

### Erroneous unit tests

An erroneous unit test may fail even if the code being tested is correct. A common error is for a programmer to assume that a failing unit test means that the code being tested has a bug. Such an assumption may lead the programmer to spend time trying to "fix" code that is already correct. Good practice is to inspect the code of a failing unit test before making changes to the code being tested.

## 13.16 Constructor overloading
- Programmers often want to provide different initialization values when creating a new object. A class creator can overload a constructor by defining multiple constructors differing in parameter types. When an object is created with the new operator, arguments can be passed to the constructor. The constructor with matching parameters will be called.
- ==If a programmer defines any constructor, the compiler does not implicitly define a default constructor, so good practice is for the programmer to also explicitly define a default constructor so that an object creation like `new MyClass()` remains supported.==

## 13.7 Objects and references
- A reference is a variable type that refers to an object.
- Variables of a class data type (and array types, discussed elsewhere) are reference variables.
- Think of string.  The reference is to the first memory location.  When a class is created it reserves the needed memory, 
- ==The new operator allocates memory for an object, then returns a reference to the object's location in memory. Thus, `travelTime = new TimeHrMin();` sets travelTime to refer to a new TimeHrMin object in memory. travelTime now refers to a valid object and the programmer may use travelTime to access the object's methods. The reference variable declaration and object creation may be combined into a single statement: `TimeHrMin travelTime = new TimeHrMin();`==
- ![[Pasted image 20251120140358.png]]

## 13.19 the "this" implicit parameter
- implicit parameter is String in String.concat().  Java uses String as the first parmeter.
- in a class with a method like below, the sideLength parameter in the setSidlength method update the objects sideLength field.  To ke
