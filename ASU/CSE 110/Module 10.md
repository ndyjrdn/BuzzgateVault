## Arrays
## 10.1 Array Concept
- An array is an ordered collection of variables (elements).  All elements in the array have the same data type and name.  Elements are accessed by integer index indicating their position in the array relative to the first element (starting at 0)
	- TLDR: an array is a
		- set of variables (elements)
		- with same name
		- and same data type
		- all located contiguously in memory (providing very fast access)
		- each element is accessed by an integer **index**

## 10.2 Arrays
### instantiation
- new dataType [array size]
- new int[5] 
	- creates an array with 5 elements
- int[] samples = new int[5]; 
	- Use like this - creates a new array names samples that contains 5 ints
-  You can declare an array (int[] gamesScores;) and then allocate it later (gameScores = new int[4];) 
	- Good practice is to do both at the same time IF the size in know 

- The accessing index is an expression but is also always an integer.  The means you can have calculation in the index (ie oldestPerson = [nthPerson-1])

### loops and arrays
- Can store user input in an array looping over nextInt()
```
System.out.println("Enter " + NUM_ELEMENTS + " integer values...");
      for (i = 0; i < userVals.length; ++i) {
         userVals[i] = scnr.nextInt();
         System.out.println("Value: " + userVals[i]);
      }
```
- .length returns the number of elements userVals.length
- 
### initialization
- default initialization for ints and floating point arrays is 0 for each element,   booleans defauls to Fales
- Can be initiated at creation 
	- int[] myAray={5,7,9};
		- Creates an array of 3 ints with those number

## 10.3 Array iteration drill
## 10.4 iterating through arrays
### Common loop structure:
```
// Iterating through myArray
for (i = 0; i < myArray.length; ++i) {
   // Loop body accessing myArray[i]
}
```

## 10.5 multiple arrays
## 10.6 Swapping 2 variables
- use temp variable to hold one val while assigning to the other then assign the temp value the other array

## 10.7 Using a loop to modify or copy an array

## 10.8 debugging example
## 10.9 2 dimensional arrays
 ==notes for tests:  instantiation of variables and arrays
 This chapter video starts with a good array reveiw==
 declaring a 2d array
 ![[Pasted image 20251110120046.png]]
 ![[Pasted image 20251110120129.png]]
 ![[Pasted image 20251110115934.png]]
 ![[Pasted image 20251110120446.png]]
 - the .length of a 2d array is the number of rows 
 - the data[row].length gives the number of columns
 - 
 ```Syntax example
 import java.util.Scanner;

public class ArraysKeyValue {
   public static void main (String [] args) {
      Scanner scnr = new Scanner(System.in);
      final int NUM_ROWS = 2;
      final int NUM_COLS = 2;
      int [][] milesTracker = new int[NUM_ROWS][NUM_COLS];
      int i;
      int j;
      int maxMiles;
      int minMiles;

      for (i = 0; i < milesTracker.length; i++){
         for (j = 0; j < milesTracker[i].length; j++){
            milesTracker[i][j] = scnr.nextInt();
         }
      }

      maxMiles = milesTracker[0][0];
      minMiles = milesTracker[0][0];
//look here
********************************************
*********************************************
       for (i = 0; i < milesTracker.length; i++) {
         for (j = 0; j < milesTracker[i].length; j++) {
            if(milesTracker[i][j] > maxMiles){
               maxMiles = milesTracker[i][j];
            }
            if(milesTracker[i][j] < minMiles){
               minMiles = milesTracker[i][j];
            }
         }
       }
  **********************************************
  **********************************************     

      System.out.println("Min miles: " + minMiles);
      System.out.println("Max miles: " + maxMiles);
   }
}
 ```

## Enhanced for loop arrays
- aka for each loop
- declares a loop variable with scope limited to the loop.
- loop var is assigned after each element is visited
- only for loops that run 0 - array.length
![[Pasted image 20251110145948.png]]
See above ☝️  

- decreased the amount of code needed to iterate an array enhncing readability and intention
- You can't use the loop variable to update the value in the array
-
## 10.11 example
## 10.12 example
## 10.13 Array parameters
# ==this is a worked example.  Good examples of many concepts here for review.==

[[Code Example 1]]  

- An array is passed to a method by passing a reference to the array. The array reference is copied to the method's parameter, so a method can modify the elements of an array argument.
- ==A common error is to assign a method's array (or object) parameter believing that assignment will update the array argument.==
- 
![[Pasted image 20251110153849.png]]

## 10.14 perfect size arrays
- Because the names of the days of the week are also unlikely to change, the array should be constant. Ex: `final String[] daysOfWeek = {"Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"};` An array that contains the list of cities where a company has locations would not be perfect size because companies can both add and subtract locations over time.

 - Takes a minute to get my head around.  
	 - This is about creating arrays in methods.   If an array is created from a method AND the size is not provided.  it's a perfect array meaning that the returned array will have the number of elements that are available in the method.  no more or less.

## 10.15 array algo example
