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
	2. names of Args and paarams
1. The param vars are assigned values in the order the arguments are listed.