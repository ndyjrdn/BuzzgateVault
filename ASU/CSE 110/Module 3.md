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
	- 