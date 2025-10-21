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
	- 
	