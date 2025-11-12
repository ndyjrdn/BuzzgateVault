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
- The declaration ==`ArrayList<Integer> vals = new ArrayList<Integer>()`== creates reference variable vals that refers to a new ArrayList object consisting of Integer objects
- ArrayList does NOT support primitive types
- ![[Pasted image 20251112102615.png]]
- ![[Pasted image 20251112102638.png]]
- 0 based index like an array
- ==An ArrayList is one of several Collections supported by Java for keeping groups of items. Other collections include _LinkedList_, _Set_, _Queue_, _Map_, and many more. A programmer selects the collection whose features best suit the desired task. For example, an ArrayList can efficiently access elements at any valid index but inserts are expensive, whereas a LinkedList supports efficient inserts but access requires iterating through elements. So a program that will do many accesses and few inserts might use an ArrayList.==

## 11.7 How do we declare and create ArrayList
```
import java.util.ArrayList;
```
ArrayList is a **generic type**

- An ArrayList, like an array, is a kind of container for other types. 
- IE An array of integers (int[ ]) is a container for int values
- it is not specialized to store values of any specific type

```
ArrayList<String> names = new ArrayList<String>();
```

## 11.8 How to access ArrayList Elements
-  Use the add method To add an element to an ArrayList.
- Use the get method To retrieve an element from an ArrayList.
- There is also a set method that will allow you to store a new element at a specified index in the ArrayList.
-[[ArrayList Methods]]


## 11.9 inserting and removing ArrayList elements
- Use the remove method To remove an element from an ArrayList.
	- the remove method automatically moves all the elements beyond the removal index to the next lower index

## 11.10 ArrayList Video
- can use enhanced for loops 
- Can be passed to a method
![[Pasted image 20251112113722.png]]

## 11.11 Arrays and arraylists
	“Code is like humor, when you have to explain it, it’s bad” - Cory House

### Array examples
```
// <data type>[] <Array name> = new <data type>[<size of Array>];

// Example 1D Array:
int[] arr = new int[5];      // here we have 5 elements

// Example 2D Array:
int[][] arr2 = new int[5][2] // here we have 5 rows and 2 columns
```

### Arraylist examples
```
import java.util.ArrayList;
...

// ArrayList<Reference Type> myArr = new ArrayList<>();

// Example of creating/instantiating an ArrayList of type Integer:
ArrayList<Integer> myList1 = new ArrayList<>();

// Example of creating/instantiating  an ArrayList with some initial elements:
ArrayList<Integer> myList2 = new ArrayList(Arrays.asList(1,2,3,4,5));

// Example of creating/instantiating  an ArrayList of some custom class type:
// Lets' say we have a class called Employee
ArrayList<Employee> myList3 = new ArrayList<>();
// This means that each of the element in myList3 will be an object of class Employee
```

#### When to use Array and ArrayList?

Use Arrays when you know the number of elements needed to perform certain tasks, and the number of element will not change while the program is running. The ArrayList is used for the cases when you don’t know how many elements you may end up adding to the data structure in advance.

## 12.1 Output and input streams
### PrintStream and System.out

- Programs need a way to output data to a screen, a file, or elsewhere. The PrintStream class provides several methods for writing data to output. Internally, a PrintStream normally places data into a temporary storage memory region, known as a buffer, and the system then outputs the buffer at various times.
- System.out is a predefined PrintStream object that is associated with a system's standard output, usually a computer screen.
- The InputStream class provides several read() methods for extracting bytes of data from an input source.
- System.in is a predefined InputStream object that is associated with a system's standard input, usually a keyboard.
- ==When using an InputStream, a programmer must append the clause `throws IOException` to the definition of main(), as shown in the animation below. A throws clause indicates that during runtime the corresponding method may exit unexpectedly due to an exception. Ex: An exception would be thrown if a program tries to read a byte, but there was a communication error with the keyboard.==
	- ![[Pasted image 20251112115256.png]]
### 
## 12.2 Streams using strings
==A programmer can read data from a string instead of from the keyboard (standard input) by associating a Scanner object with a String. A Scanner object initialized from a String is often referred to as an input string stream.==

![[Pasted image 20251112115913.png]]

### Line-by-line input processing
A common use of string streams is to process user input line-by-line. The following program uses scnr.nextLine() to read an input line from standard input and copy the line into a String. The statement inSS = new Scanner(lineString); creates a Scanner object using the String lineString. Afterwards, the program extracts input from the inSS stream using the next() and nextInt() methods.
![[Pasted image 20251112120109.png]]

- An output string stream is a stream that can write to a String instead of to standard output. An output string stream allows a programmer to build and format a String before outputting to a file or the screen.
- An output string stream is created using both the StringWriter and PrintWriter classes, which are available by including: `import java.io.StringWriter;` and `import java.io.PrintWriter;`. The StringWriter class provides a character stream to output characters. The PrintWriter class augments character streams, such as StringWriter, with print() and println() methods to output various data types, like int, double, and String, in a manner similar to System.out.

## 12.3 File input
