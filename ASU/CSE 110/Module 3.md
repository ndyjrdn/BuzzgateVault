# Data types Expressions and variables Part 2

## 3.1 Using Math Methods

- a standard Math class has about 30 math ops called methods. This is part of Java's standard library so no import needed.

Table 3.1.1: A few common methods from the standard Math class.
[[Math Methods]]


|Method|Behavior|Example|
|---|---|---|
|sqrt(x)|Square root of x|Math.sqrt(9.0) evaluates to 3.0.|
|pow(x, y)|Power:|Math.pow(6.0, 2.0) evaluates to 36.0.|
|abs(x)|Absolute value of x|Math.abs(-99.5) evaluates to 99.5.|

## 3.2 Interger division and Modulo

Int always round down.  Any fraction less than 1 is 0
int division by 0 will be an error

Modulo (represented for %) is the remainder.
	IE 23 % 10 = 3

## 3.3 Type conversions

- Converting a number from one type (int) to another (float)
- for arithmetic if either is a double both are converted automatically
- for assignment the value is converted to the type the variable without loss of precision.

### Type casting
- precede a value with a type to cast it to another type 
	- (double)7 converts int 7 to 7.0
- A common error is to accidentally perform integer division when floating-point division was intended. The program below undesirably performs integer division rather than floating-point division.
- A common error is to cast the entire result of integer division, rather than the operands, thus not obtaining the desired floating-point division.

## 3.4 Binary
 0s and 1s

# 3.5 Characters

- char data type 
- single character
- ie 'm'
- initialize with single quotes  
	- char userKey = 'a'
- To get a specific character from a string use .charAt()
	- scnr.next().charAt(0) is first letter
- Stored as a number under the hood.  (ascii coding)
[[ASCII Symbols]]

[[Escape sequences]]

### outputting multiple character variables with ont output statement
==A programmer can output multiple character variables with one statement as follows: `System.out.print("" + c1 + c2);`. The initial "" tells the compiler to output a string of characters, and the +'s combine the subsequent characters into such a string. Without the "", the compiler will simply add the numerical values of c1 and c2, and output the resulting sum.==

### Common errors
=using " "  instead of ' ' when assigning  a char.  But don't forget the ' ' or it will not compile

## 3.6 Strings
- a string is a sequence of characters
- a string literal surrounds a character sequence with double quotes line "Hello"

#### string variables and assignments
- a String variable is a 'reference type' so the variable refers to an object.
- an object consists of internal data items plus operations that can be performed on that data. 

#### getting a string WITHOUT whitespaces from input 
===A whitespace character is a character used to represent horizontal and vertical spaces in text, and includes spaces, tabs, and newline characters. Ex: "Oh my goodness!" has two whitespace characters, one between h and m, the other between y and g.
Below shows the basic approach to get a string from input into variable userString. The approach automatically skips initial whitespace, then gets characters until the next whitespace is seen.

==userString = scnr.next();==

#### getting a string WITH whitespaces from input 

==Sometimes a programmer wishes to get whitespace characters into a string, such as getting a user's input of the name "Franklin D. Roosevelt" into a string variable presidentName.
For such cases, the language supports getting an entire line into a string. The method scnr.nextLine() gets all remaining text on the current input line, up to the next newline character (which is removed from input but not put in stringVar).==

Mixing next() and nextLine() can be tricky, because next() leaves the newline in the input, while nextLine() does not skip leading whitespace.

![[Pasted image 20251019150052.png]]


## 3.7 integer overflow
==An overflow occurs when the value being assigned to a variable is greater than the maximum value the variable can store.==

an int can only store number up to around 2 billion.  After that the binary representation is too long.  Switch to long type.  The issue could be in interim steps so watch out.

## 3.8 Numerid data types
[[Integer data types]]
short and byte are rarely used except for managing memory if needed
[[Floating point data types]]
float here is similar to short and byte above
Overflow in a float is infinity

![[{73EFF3A7-D7BA-4D33-84F6-A7B5B3FF1BBB}.png]]

## 3.9 Random number
- the Random class provides methods that return a random integer 
```
import java.util.Random;

public class ThreeRandomValues {
   public static void main(String[] args) {
      Random randGen = new Random();  // New random number generator

      System.out.println(randGen.nextInt());
      System.out.println(randGen.nextInt());
      System.out.println(randGen.nextInt());
   }
}
959650663
324135575
1735989143
```
- The statement `import java.util.Random;` enables use of the Random class. The statement 
- `Random randGen = new Random();` creates a new random number generator object named randGen. 
- The method call randGen.nextInt() can then be used to get a random integer ranging from  to .

randGen.nextInt(10) will return a random value from  0 to 9

to return a random value from a range 
![[Pasted image 20251019153527.png]]

#### pseudo-random
random numbers are actually calculated based on the previous number.  The first is based on the current timestamp(seed).  We can set the see when the Random method is called like Random randGen = new Random(15);  This enables reproducibility in 'random' values


## 3.10 Debugging

**Debugging** is the process of determining and fixing the cause of a problem in the program (also called **troubleshooting**)
 - predict possible cause
 - test
 - repeat

==Note that a temporary statement commonly has a "FIXME" comment to remind the programmer to delete this statement.==
Debug or print statement

- Manually set a variable to a value.
- Insert print statements to observe variable values.
- Comment out unused code.
- Visually inspect the code (not every test requires modifying/running the code).
