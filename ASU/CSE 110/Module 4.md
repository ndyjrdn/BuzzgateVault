## 4.1 
Printing to the console.  
System.out.print("test"); no new line.  just tacks the next output on the end

System.out.print("test\n");
System.out.println("test"); These do the same thing.  print the text and return to the beginning of the next line.


## 4.2 output formatting

input, output and formatting

![[{875FB592-81F5-4D23-89D3-ECDA6EC13646}.png]]

![[{259D5729-6504-44C9-BB72-0E2BA10A1E33}.png]]
[[Format specifiers]]
#### printf() and format() methods

![[{96B2FAD5-2C99-48E5-8A2B-47C7285A351E}.png]]

### Floating point values

sub-specifier is the number between the % and the format.  IE "%.1f" prints a float with 1 digit after the decimal
[[Format specifiers]]

#### Integer Values

#### Strings

#### Flushing output
System.out.flush()

## 4.3 Getting inputs
- Import scanner
	- Import java.util.Scanner;

> - Instantiate
	- Scanner input = new Scanner(System.in);
		- Scanner object
		- Named input
		- 'New'
		- System.in connects to input
- ![[{0E9BF5B7-CC85-46AC-A602-577523C471ED}.png]]


## 4.4 introduction to Entrepreneurial Mindset
	All engineers are entrepreneurs
	Skillset = power
	mindset = direction
 - Curiosity
 - Connections
 - Create Extraordinary Value
Humans have problems
Take a human centered approach

==Best Practice: fully understand the problem you're trying to solve by talking to your users, manually verifying and testing your program, and getting feedback to make sure your program is correct and useful every step of the way!==

## 4.5 Vending Machine Example
understand the problem
	- Inputs
	- Outputs
```
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner in = new Scanner(System.in);
    // declare variables
		int billDenomination = 0;
		int itemPrice = 0; 
		int changeDue = 0;
		int dollarCoins = 0;
		int quarters = 0;

		// get inputs
		System.out.print("Enter denomination of bill -->");
		billDenomination = in.nextInt();
		System.out.print("Enter item price in pennies-->");
		itemPrice = in.nextInt();
		
		// Calculate the change due
		changeDue = 100 * billDenomination - itemPrice;
		// Calculate the number of dollar coins to return
		dollarCoins = changeDue / 100;
		changeDue = changeDue % 100;
		// Calculate the number of quarters to return
		quarters = changeDue / 25;

		// output results
		System.out.printf("Returning %d dollar coins", dollarCoins);
    System.out.printf(" and %d quarters.%n", quarters);
  }
}
```

## Chapter 5
#### 5.1 Why is sequence important
The computer executes instructions in sequence
Must declare a variable before using it.

#### 5.2 Common patterns with variables
- Incrementing: typically add 1
	- pizzas++; // Using Java's Increment Operator
	- pizzas += 1; // Using Java's Addition Assignment Operator
- Decrementing: typically subtract 1
	- breadsticks--; // Using Java's Decrement Operator
	- breadsticks -= 1; // Using Java's Subtraction Assignment Operator
- Accumulate a total
	- 
#### 5.3 Swap the values or 2 variables

What we need is a place to temporarily store one of the values.  Variables store values!
Figure 5.3.1: Try this:
int temporaryValue = month;   // Save value of month in temporary_value
month = day;                  // Assign value of day to variable month
day = temporaryValue;         // Assign saved value of month to day

This is a very common pattern for swapping values using a temporary variable.

#### 5.4 Input->Processing -> Output Pattern

how to program with this (input-process-output) pattern
- Generalization: Flexible and scalable
- Abstraction:  methods/functions (Didn't use these terms but...)
- Maintainability: readable, scale, correct
- Modular

#### 5.5 how can we trace a program
 🤖 Sequence matters for this
 - Predictability
#### 5.6 Strings & string methods
- Strings are not primitive (built in) types in Java
-  String literals use ""
	- String name = "Bob Smith";
-  + Concatenation
	- ![[Pasted image 20251021175929.png]]
	- next() - next word
	- nextLine() - line to next newline
	- ![[{7D859D61-E132-42B4-8D02-B1270DBE1D13} 1.png]]
	- Strings are a sequence of chars
	- charAt() - extracts a character from a specific index (starting with 0)
	- Length() - Returns the number of characters in the string (including spaces)
	- substring() - Pull out the chars in the range of inputs.
	- indexOf() - Returns the index number of a letter in a sequence
	- .equals() for strings is T/F if they match (T) else (F)
	- compareTo() - evaluates for alphabetical order
		- - if the it comes before the first
		- + if after
		-  0 if they are the same
		- 🚩Capitals come before lowercase
		
## 9.4 For loops

- counter shortcuts
	- x=x+1
	- x +=
	- x++
	- y = y-1
	- y =-
	- y--
		- i++ increments AFTER the body runs
		- ++i increments BEFORE the body is run


- for loops are counter controlled loops
	- for: key word
	- initialization : initialized counter
	- condition: evaluates T/F
	- update: updates counter
	- body:  instructions
```
for(initialization; condition; update){
	body
}

for(number = 1; number < 4; number++){
	do stuff
	// starting with number = 1 until 4 counting by ones  
}
```
![[Pasted image 20251105174051.png]]

## 9.5 more loop examples
- general preference is to start is i=0 and i < N rather than i=1 due to the 0 index array counting in Java and other languages.

## 9.6 loops and strings
## 9.7 Nested loops
- inner loop is in the body of the outer loop
- 
## 9.8 Stacked loops
## 9.9 Developing programs incrementally
- Do a little, test and fix, do a little more, test and fix...etc
## 9.10 Break and continue
- A break statement in a loop causes an immediate exit of the loop.
- A continue statement initiates a jump to the condition check

## 9.11 Variable name scope
- A variable is only valid in it's scope.  the scope applies to the block in which it was declared.  
- A block is a brace enclosed sequesnce of statements {}
- A common error is to declare a variable inside a loop whose value should persist across iterations.

## 9.12 Enumerations
- ==an enumeration type (enum) declares a name for a type and possible values for that type==
```
public enum identifier{enumerator1, enumerator2, ...}
```
			- Items in the {} are named constants
			- they are NOT assigned a numeric values
			- referenced by defined names
			- Can be used like other data types
- A state machine is used in programs where the program changes 'state' of a thing based on conditions.
	- Basically an if/else ladder to determine the state.
	- Works in here as you can enumerate a variable (lightsaber) and assign it different colors based on criteria.  The state machine is the algorithm that updates the state based on the conditions.
		- A programmer must include both the enumeration type and the enumerator within that type, as in 
		- `lightVal = LightState.RED;`
		- A common error is to omit the enumeration type in an expression. For example, the statement 
		- `lightVal = RED;`   results in a compilation error.==
	==One might ask why the light variable wasn't simply declared as a string, and then compared with strings "GREEN", "RED", and "YELLOW". Enumerations are safer. If using a string, an assignment like `light = "ORANGE"` would not yield a compiler error, even though ORANGE is not a valid light color. Likewise, `light == "YELOW"` would not yield a compiler error, even though YELLOW is misspelled.==

## 9.13 example
## 9.14 example

## 9.15 Methods with loops
