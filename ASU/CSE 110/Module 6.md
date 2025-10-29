## 7.1 User defined method basics

- name methods verbs that say what the do
- A method is a names list of statements
- a method definition: a new methods name and block of statements
- A method call is an invocation of the methods name causing it to execute
- A block is a list of statements surrounded by {}
- methods must be defined in a class

```
 public class PizzaArea { 
   public static double calcPizzaArea() {
      double pizzaDiameter;
      double pizzaRadius;
      double pizzaArea;
      double piVal = 3.14159265;

      pizzaDiameter = 12.0;
      pizzaRadius = pizzaDiameter / 2.0;
      pizzaArea = piVal * pizzaRadius * pizzaRadius;
      return pizzaArea;
   }

   public static void main(String[] args) {  
      System.out.println("12 inch pizza is " +   
       calcPizzaArea() + " inches squared"); 
   }
}
```

- public and static are access modifiers
	- public means the method can be called from any class
	- static means it only uses values passed to it.
- A method can return one value via a return statement
- a parameter is an input to the method
	- Could be 0 or several (comma separated)
- an argument is the value provided to the parameter

practice methods 
```
import java.util.Scanner;

public class CalcPyramidVolume {

   public static double pyramidVolume(double userLength, double userWidth, double userHeight){
      double vol;
      double baseArea;
      
      baseArea = userLength * userWidth;
      vol = (baseArea * userHeight) * 1/3 ;
      return vol;
   }

   public static void main (String [] args) {
      Scanner scnr = new Scanner(System.in);
      double userLength;
      double userWidth;
      double userHeight;

      userLength = scnr.nextDouble();
      userWidth = scnr.nextDouble();
      userHeight = scnr.nextDouble();

      System.out.println("Volume: " + pyramidVolume(userLength, userWidth, userHeight));
   }
```

## 7.2 Print methods

- A method that just prints and does not return anything uses the keyword void
- Methods that use void are unsurprisingly called void methods
- One benefit of a print method is that complex output statements can be written in code once. Then the print method can be called multiple times to produce the output instead of rewriting complex statements for every necessary instance. Changes to output and formatting are made easier and are less prone to error.

## 7.3 methods with no parameters and return value

🚩🚩If there is not already a method to do what we want,
then we should define a method to do it.🚩🚩
![[Pasted image 20251023201137.png]]

Notice that a method definition may include some access modifiers which will be discussed in more detail later. We will be using the public static access modifiers for now. A method definition will always have these parts:
1.  ==return type== - the type of value this method will return
2. ==methodName== - the name for this list of instructions
3. ==(parameterList)== - describing the arguments that must be passed to this method
4. =={methodBody}== - the list of instructions to execute when this method is called

public static void printBunny() {
   print(" (\\(\\   ")
   print(" (-.-)    ")
   print(" O_(\")(\") ")
}
 - no return type defined
 - no parameters

### Mechanics of method calls (UDM)

## 7.4 Define methods with parameters
-  Arguments are the values passed to methods
-  Parameter is the value needed.  The variable that stores the arguments

### Misconceptions
	1. order of Args and params
	2. names of Args and params
1. The param vars are assigned values in the order the arguments are listed.
2. Names of params doesn't matter.  The order matters

### Mechanics of method calls (UDM)
### Call stack

The stack is was also called the local variable Local as opposed to global memory.   This helps define scope of variables and methods

When a method is called 5 things happen
 1. Stack frame is created in stack memory
 2. Return point is recorded in stack frame
 3. Local variables are created from method (local is scoped to the method) 
 4. Parameter variables are assigned (variable values are populated)
 5. Instructions are executed

When a method finishes 3 things happen:
1.  Local variables are removed from the stack
2. Stack is removed
3. Control returned to main

## 7.5 Reasons for defining methods

- We can name information - in this case, a series of actions
- ==Improve readability==
	- methods may add lines of code because of formatting/lniting
- ==Modular and incremental dev==
	 - Modular development is the process of dividing a program into separate modules that can be developed and tested separately and then integrated into a single program.
	- Incremental development is a process in which a programmer writes, compiles, and tests a small amount of code, then writes, compiles, and tests a small amount more (an incremental amount), and so on.
	- A method stub is a method definition whose statements have not yet been written. 
	- ### Example stub

```
public static double calcMpg(double distMiles, double gasGallons) {
      System.out.println("FIXME: Calculate MPG");
      return 0.0;
   }
//Essentially a placeholder for planning a future method

```

- Avoid writing duplicate code

### The skill of decomposing a program's behavior into a good set of methods is a fundamental part of programming that helps characterize a good programmer. Each method should have easily-recognizable behavior, and the behavior of main() (and any method that calls other methods) should be easily understandable via the sequence of method calls. ==A general guideline (especially for beginner programmers) is that a method's definition usually shouldn't have more than about 30 lines of code, although this guideline is not a strict rule.==

## 7.6 Writing mathematical methods

 - It is valid and expected to break methods deeper and call methods inside of methods
## 7.7 Scope of variable method defs
- when java needs a variable value in a function it runs a scope resolution process to first look for it in the local scope (the function scope and value) and if it doesn't find it there it checks the global variable.
- the defined variable or method is only visible to part of the program.  The Scope
- A variable declared in a method is only available to the method.  
- A variable declared within a class but outside any method is called a _class member variable_ or field, in contrast to a local variable defined inside a method. A field's scope extends from the class's opening brace to the class's closing brace, and reaches into methods regardless of where the field is declared within the class. (Global Variable or field)
- A local variable's scope starts when it's declared.
- A method also has scope, which extends from the class's opening brace to the class's closing brace. Thus, a method can access any other method defined in the same class, regardless of the order in which the methods are defined.

## 7.8 what can we do with a method

1. Define it
2. Call it.
- The power of methods comes from how we use them.
	- Simplify design, construction, testing and debugging
		- Methods allow
			- Named operations
			- Deconstruct complex into simple parts
			- build complex programs out of simple pieces


	
designing vs writing programs
	- diving right in and coding is fun and you be educational but it leads to problems...no shit
	- Take time to think about the problem
	- design the solution
	- THEN start coding
	- A good program is full or functions

-Pyramids

- public is a visibility modifier meaning it can be used by any method in the program
- static operates on the class not the  
- Non-static methods create an object and then do stuff 
	- Scanner scnr = new Scanner(System.in);
	- This is a non_static method because the new Scanner is an object.
-
## 7.9 Method name overloading

There CAN be 2(or more) methods with the same name with differing parameters - The compiler will figure it out based on the arguments given

## 7.10 How methods work

## 7.11 common errors
- Copying code and forgetting to update it for the new context
- Returning the wrong value
-  Forgetting/failing to return a value

## 7.12 Using scanner in methods
- A program should use only one scanner per input stream
- you pass the scanner as a argument
	- ==public static double getPizzaCalories(Scanner scnr)==
- 
- 