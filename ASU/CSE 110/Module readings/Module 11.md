## 11.1 What are value types
- There are 2 types in java:
	- Value types
	- Reference types
- All primitive types are value types
- Value types variables always store a value of that type
- Assignment statement stores a value in the variable.
	- only 1 per value type
	- when a new value is assigned it replaces the former
	- 
	## 11.2 Value Type assignment
	1. A variable is a name that refers to a location in computer memory where a value is stored.
	2. A value type variable stores a value of that type.
	3. An assignment statement stores a value in a variable.
## 11.3 What are reference types
- all non-primitive types are reference types
- ==A variable of a non-primitive type must store a reference to an object of that type, or the special null reference. A variable of type Scanner always stores a reference to a Scanner object, or it stores a null reference. A null reference means that the variable does not refer to any object at this time.==
-  Reference types can store a reference to a variable of that type OR null
-  if not initialized when declared they default to null

## 11.4 primitive and reference types
### Wrapper classes
Java variables are one of two types.
- A primitive type variable directly stores the data for that variable type, such as int, double, or char. Ex: `int numStudents = 20;` declares an int that directly stores the data 20.
- A reference type variable can refer to an instance of a class, also known as an object
- ==Java provides several wrapper classes that are built-in reference types that augment the primitive types. The Integer data type is a built-in class in Java that augments the int primitive type. Ex: `Integer maxPlayers = 10;` declares an Integer reference variable named maxPlayers that refers to an instance of the Integer class, also known as an Integer object. That Integer object stores the integer value 10.==
- 
- ![[Pasted image 20251112094948.png]]
- ==Many of Java's built-in classes, such as Java's Collection library, only work with objects. For example, a programmer can create an ArrayList containing Integer elements, e.g., `ArrayList<Integer> frameScores;` but not an ArrayList of int elements. Wrapper classes allow the program to create objects that store a single primitive type value, such as an integer or floating-point value. The wrapper classes also provide methods for converting between primitive types (e.g., int to double), between number systems (e.g., decimal to binary), and between a primitive type and a String representation.==
- Wrapper classes ^^ can be used in expressions just like primitives
- **Wrapper classes are immutable**
	- a programmer cannot change the object via methods or variable assignments after object creation.
- Wrapper classes have the same size limits as primitives
- comparing  reference variables with == or != compares whether they refer to the same object, not whether the values are the same.
	- think of String.   String == String doesn't work. String.equals(String) ;)
- ![[Pasted image 20251112100157.png]]
- Reference variables of wrapper classes can also be compared using the equals() and compareTo() methods. These method descriptions are presented for the Integer class, but apply equally well to the other wrapper classes. ==Although the use of comparison methods is slightly cumbersome in comparison to relational operators, these comparison methods may be preferred by programmers who do not wish to memorize exactly which comparison operators work as expected.==

## 11.5 Wrapper class conversions
- Autoboxing is the automatic conversion of prim to wrapper
- Unboxing is automatic convertion from wrapper to prim
### Converting wrapper class opbects to primitive types
![[Pasted image 20251112101031.png]]
	The Character and Boolean classes support the charValue() and booleanValue() methods, respectively, which perform similar functions.
	==Several of these methods are static methods, meaning they can be called by a program without creating an object. To call a static method, the name of the class and a '.' must precede the static method name, as in `Integer.toString(16);`. ==
	
![[Pasted image 20251112101815.png]]


## 11.6 ArrayList
- ArrayList works like a resizable array
- An ArrayList is an ordered list of reference type items that comes with Java. Each item in an ArrayList is known as an element. The statement `import java.util.ArrayList;` enables use of an ArrayList.
The declaration ==`ArrayList<Integer> vals = new ArrayList<Integer>()`== creates reference variable vals that refers to a new ArrayList object consisting of Integer objects

