## 2.1 Data types
### A Data Type is an encoding of a set of values so that the computer can store and manipulate them

- Transistors are switches (on or off)
- Numbers are encoded in binary using base 2
- Floats are encoded in binary with a special layout
- Text is encoded in binary representing the ascii numeric symbol in binay.
- ==ASCII and Unicode are 2 systems for encoding and decoding text using numbers==
- 
- 
### Pictures as data
![[{B1326C45-DD4B-46BF-B60F-31E908BDD95C}.png]]

0 = black 255 = black

![[{6745CAC5-0CF0-4C1A-9D3F-A054157F0C09}.png]]

- ==Data type is a way to encode some type of value so that a computer can manipulate it using only ones and zeros==

## Common Data Types

Boolean - representing only true or false values. These are used in logic expressions and decisions.

Integer - representing positive or negative whole numbers without a fractional part. Examples: -127, 8, 65535.

Floating Point - representing positive or negative numbers with a fractional component. Examples: 3.1415, 2.0, -123.456.

String - representing textual information as a sequence of encoded characters. Examples: "Hello!", "This is a String.".

## Java primitive data types

|   |   |
|---|---|
|Type Name|Description|
|byte|Integers (whole numbers) in the range of -128 to +127|
|short|Integers in the range of -32,768 to +32,767|
|int|Integers in the range of -2,147,483,648 to +2,147,483,647|
|long|Integers in the range of -9,223,372,036,854,775,808 to +9,223,372,036,854,775,807|
|float|Real numbers in the range of ±3.40282347 x 1038 to 1.40239846 x 10-45|
|double|Real numbers in the range of ±1.7976931348623157 x 10308 to 4.9406564584124654 x 10-324|
|char|Any single character|
|boolean|Only two values: true and false|

|   |   |   |
|---|---|---|
|Type|Size (bits)|Range|
|byte|8|-128 to +127|
|short|16|-32,768 to +32,767|
|int|32|-2,147,483,648 to +2,147,483,647|
|long|64|-9,223,372,036,854,775,808 to +9,223,372,036,854,775,807|
|float|32|±3.40282347 x 1038 to 1.40239846 x 10-45|
|double|64|±1.7976931348623157 x 10308 to 4.9406564584124654 x 10-324|

==Choose int for whole numbers
In general==  

==Choose double for real numbers
In general==

 - Floats have precision to 9 digits, doubles to 17
 - Always assume the last digit is rounded
 - follow  a float with f 
	 - 3.14f -> float
	 - 3.14 -> double
- Adding _1_ to the maximum value for an **int** will **overflow** the range of valid values for that data type. In this case, Java resolves the issue in the same way that an automobile odometer would - it simply wraps back around to the minimum valid value for that type _-2147483648_.
 - ==Java's String data type is NOT primitive (hence the capital s)==
## 2.3 Expressions and Operations

![[{42862317-ECC9-4588-B138-CA7821AF3652}.png]]

![[{E1FBA93F-B347-455A-AC64-2B2DF79754E0}.png]]
- ==Expressions always evaluate to a value==
- literals are values that express a value in a literal way,.  like 123
 
Here is a list of the most common escape sequences.

|   |   |
|---|---|
|Escape Sequence|What it represents|
|\n|a Newline (or Return) character|
|\t|a Tab character|
|\"|a Double Quote mark. This is used to include a Double Quote mark as a character in a String literal. For example: we can encode the String: <br><br>  <br><br>He said "Hello!"<br><br>  <br><br>as a String literal like this:<br><br>  <br><br>"He said \"Hello!\""|
|\'|a Single Quote mark. For example, we can represent a Single Quote mark as a char literal like this:<br><br>  <br><br>'\''<br><br>  <br><br>Note that there are three single quote marks in the char literal above.|
|\\|a Backslash character. Because Java assumes that a Backslash in a String literal is the start of an escape sequence, we need this special escape sequence to represent a single Backslash character in a String literal.|

  

## 2.4 Operators
Here is a list of the Java math operators.

|   |   |
|---|---|
|Operation|Java Operator|
|Addition|+|
|Subtraction|-|
|Multiplication|*|
|Division|/|
|Modulus|%|
- ==Operators operate on operands==
- ==Operators are instructions telling the computer to do some work==
- ==Integer Division An int divided by an int will always* give an int result in Java.==

## 2.5 how is an expression evaluated to a value

- ==compound expressions are expressions composed of sub-expressions==
	- When there are multiple steps IE (3+5)*2 or 3+5 *2  
	the computer will do the first step, store the output, then use that stored output on the next step etc.
	- 3 + 5 \* 2 is a series of instructions.  
	- ==An Expression is a list of instructions for the computer to follow to compute a value
	- 
## 2.6 String Expressions
- ==Escape Sequence is a combination of symbols, starting with a backslash that denotes a special character lake a tab or a newline in a string literal==
- 
	Here is a list of the most common escape sequences.

|                 |                        |
| --------------- | ---------------------- |
| Escape Sequence | What it represents     |
| \n              | Newline character      |
| \t              | Tab character          |
| \"              | Double Quote character |
| \'              | Single Quote character |
| \\              | Backslash character    |
-  ==concatenation is building longer Strings out of shorter Strings.==

## 2.7 type casting

- Widening casts convert a data type in to a wider one IE int -> float
- If needed, Java can auto cast IE int 3 + double 2.5 evaluates to 5.5  converting the 3 to a double and then calculating
- ==Java cannot perform operations with operands from different types==
- ==Implicit Cast: Java will automatically cast a value of a narrower type to an equivalent value of a wider type.
- if we explicitly cast from double to int and decimals will be dropped.  
- casting syntax:
	(<dataTypeToCastTo\>)valueToCast 
	(int) 3.1415
	(float)(3.1415 * 2.275 * 2.275)

## How can we convert data types 
To convert from string to numeric we can use parse methods.  IE
	- Interger.parseInt
	- Float.parseFloat
	- Double.parsDouble
- Cast operations and parse methods are expressions - Expressions always evaluate to a value
- 

## 2.9 How are expressions used

- Write mathematical expressions, using literal values, then output the result to the console
- 🤖 repl.it  (java scratch pad)
-  

## 2.10 Variables and assignments (general)

- ==variable== is a named item
- an ==assignment== assigns a value to a variable 

🚩= is not equals
In programming, = is an assignment of a left-side variable with a right-side value. = is NOT equality as in mathematics. Thus, x = 5 is read as "x is assigned with 5", and not as "x equals 5". When one sees x = 5, one might think of a value being put into a box.

- Increasing a variable's value by 1, as in x = x + 1, is common, and known as incrementing the variable.

## 2.11 Variables (int)

- a variable declaration is a statement that declares a new variable specifying the var's name and type  
- Allocation is the process of determining a suitable memory location to stoire data lik variables
	-  The programmer must declare a variable before any statement that assigns or reads the variable, so that the variable's memory location is known
- Assignment statements assign a value to a variable.
- initializing variables in assigning the first value which can happen at declaration like
   int avgLifespan = 70;
## 2.12 Identifiers
- A name for a variable or method (or function I assume) is called in identifier.
	- They must be letters \_, $, or numbers
	- Can't start with a number
	- Case sensitive in java

Java reserved words / keywords

|   |   |   |
|---|---|---|
|abstract  <br>assert  <br>boolean  <br>break  <br>byte  <br>case  <br>catch  <br>char  <br>class  <br>const  <br>continue  <br>default  <br>do  <br>double  <br>else  <br>enum  <br>extends|final  <br>finally  <br>float  <br>for  <br>goto  <br>if  <br>implements  <br>import  <br>instanceof  <br>int  <br>interface  <br>long  <br>native  <br>new  <br>package  <br>private  <br>protected|public  <br>return  <br>short  <br>static  <br>strictfp  <br>super  <br>switch  <br>synchronized  <br>this  <br>throw  <br>throws  <br>transient  <br>try  <br>void  <br>volatile  <br>while|

## 2.13 arithmetic expressions

### Basics

An expression is any individual item or combination of items, like variables, literals, operators, and parentheses, that evaluates to a value, like 2 * (x + 1). A common place where expressions are used is on the right side of an assignment statement, as in y = 2 * (x + 1).

A literal is a specific value in code like 2. An operator is a symbol that performs a built-in calculation, like +, which performs addition. Common programming operators are shown below.

## 

Table 2.13.1: Arithmetic operators.

| Arithmetic operator | Description                                                                                                |                                                                                                                                                                                                |
| ------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| +                   | The addition operator is +, as in x + y.                                                                   |                                                                                                                                                                                                |
| -                   | The subtraction operator is -, as in x - y. Also, the - operator is for negation, as in -x + y, or x + -y. |                                                                                                                                                                                                |
| *                   | The multiplication operator is *, as in x * y.                                                             |                                                                                                                                                                                                |
| /                   | The division operator is /, as in x / y.                                                                   |                                                                                                                                                                                                |
| Operator/Convention | Description                                                                                                | Explanation                                                                                                                                                                                    |
| **( )**             | Items within parentheses are evaluated first                                                               | In 2 * (x + 1), the x + 1 is evaluated first, with the result then multiplied by 2.                                                                                                            |
| **unary -**         | - used for negation (unary minus) is next                                                                  | In 2 * -x, the -x is computed first, with the result then multiplied by 2.                                                                                                                     |
| *** / %**           | Next to be evaluated are *, /, and %, having equal precedence.                                             | (% is discussed elsewhere)                                                                                                                                                                     |
| **+ -**             | Finally come + and - with equal precedence.                                                                | In y = 3 + 2 * x, the 2 * x is evaluated first, with the result then added to 3, because * has higher precedence than +. Spacing doesn't matter: y = 3+2 * x would still evaluate 2 * x first. |
| **left-to-right**   | If more than one operator of equal precedence could be evaluated, evaluation occurs left to right.         | In y = x * 2 / 3, the x * 2 is first evaluated, with the result then divided by 3.                                                                                                             |

## 2.14 Arithmetic expressions (int)

- Good practice to leave a space around operators (2 + 3 ) instead of (2+3)
- a minus sign - used as a negative is a unary minus
- Compound operators are shorthand ways to update variables ie userAge +=1 is userAge = userAge + 1
- No commas

## 2.15 Example
-  Incremental development is the process of writing, compiling, and testing a small amount of code, then writing, compiling, and testing a small amount more (an incremental amount), and so on.

## 2.16 Floating point numbers (double)
- Double holds a float point point (wider that float)
- Should start floating point literals with a number left of the decimal.  ie 0.5
- Very large and small floats with use scientific notation 2.99792458E8
- in Java dividing by 0 produces Infinity or -Infinity
-  0/0 is NaN
- To print a float to 2 decimal places:
	- System.out.printf("%.2f", myFloat);
	- When outputting a certain number of digits after the decimal using printf(), Java rounds the last output digit, but the floating-point value remains the same. Manipulating how numbers are output is discussed in detail elsewhere.

## 2.17 Scientific notation for floating point literals

==Scientific notation is useful for representing floating-point numbers that are much greater than or much less than 0, such as 6.02 x 1023. A floating-point literal using scientific notation is written using an e preceding the power-of-10 exponent, as in 6.02e23 to represent 6.02 x 1023. The e stands for exponent. Likewise, 0.001 is 1 x 10-3 and can be written as 1.0e-3. For a floating-point literal, good practice is to make the leading digit non-zero.==

## 2.18 Constant Variables
🚩 ==A good practice is to minimize the use of literal numbers in code.==

- A variable name preceeded by 'final' creates a variable that is constant and can't be changed later in the script
- 