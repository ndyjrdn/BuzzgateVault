## 6.1 What is a Method

🚩a program can be viewed as a package or responsibilities
- 2 forms of responsibilities
	-  Things the program must know and remember or keep track of **VARIABLES**
	- Things the package must do, instructions is must carry out. **METHODS**
	Variables - NOUNS
	Methods - VERBS

	==A method is a name that refers to a sequence of instructions in memory. Those instructions are executed when the method is called by its name.==
	==In much the same way that a variable allows us to name a value, a method allows us to name a sequence of instructions. Both make our programs easier to design, easier to write, easier to read, easier to test, easier to debug, and easier to maintain.==
	
	- the best way to get something done in a program is to call a method that does that thing
	- 
## 6.2 how to call a method
🚩A method call has 2 major parts, the ==method name==, and the ==argument list==.
- argument lists are ALWAYS separated by commas

## 6.3 what are arguments
🚩Arguments give methods what they need
- can be literals, variables, or expressions.  All evaluate to a value
- Arguments are evaluated to values before the method is called, the values are passed to the methods
- When a method returns a value, a call to that method is an expression that evaluates to the returned value. This means that we can use a call to a method that returns a value of a given data type anywhere we can use an expression of that data type.
- We can use a call to a method that returns a value, as a sub-expression within a larger expression. Here is an example where the method call Math.sqrt(area) is a sub-expression of the larger expression 4 * Math.sqrt(area).

## 6.5 some standard library methods
- mechanics of function calls (he does say FUNCTIONS)

## 6.6 String methods

 charAt
 length
 someString.charAt(1) or someString.length()
 
 #### finding a string in a string
 indexof() returns the index where the argument starts.
 [[String methods]]
 