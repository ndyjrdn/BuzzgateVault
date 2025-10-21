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