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
- a string li