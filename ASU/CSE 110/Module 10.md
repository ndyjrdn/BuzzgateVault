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
Good algorithm examples.  
- [[print array]]
- [[print sum]]
- [[return sum]]
- [[return average]]
- [[return max]]
- [[return min]]
- [[find first]]
- [[find last]]
- [[swap by index]]
- [[bubble sort]]

## 10.16 oversize arrays
- An oversize array is an array where the number of elements used is less than or equal to the memory allocated. Since the number of elements used in an oversize array is usually less than the array's length, a separate integer variable is used to keep track of how many array elements are currently used.

## 10.17 methods with oversized arrays
- If the array size is changed by a method, then the new array size needs to be returned by the method.
- A common error is to not return the new size of an oversize array that was modified in a method.

## 10.18 comparing perfect and oversized arrays
- A method signature can tell a programmer whether a perfect size or oversize array is expected as an argument.

	- A method that expects a perfect size array as an argument will have one parameter for the array reference, but no parameter for the array size. Ex: `int findIndexMax(String[] arrayReference)` expects a perfect size array.
	- A method that expects an oversize array as an argument will have two parameters to pass the array: one for the array reference and one for the array size. Ex: `int binarySearch(String[] arrayReference, int arraySize, String searchKey)` expects an oversize array.
- The return type can also help a programmer determine whether a method uses a perfect size or an oversize array.

	- If a method returns an array reference, the method constructs a perfect size array. An oversize array cannot be constructed inside a method because the method would need to return both an array reference and array size, which is not permitted in Java.
	- If a method returns an int, the method may use an oversize array, where the return value indicates the new array size. Ex: `int removeAll(String[] arrayReference, int arraySize, String target)` removes all of the occurrences of target from an oversize array. Because the method has an arraySize parameter and returns an int, a programmer can determine that the method uses an oversize array.
![[Pasted image 20251110180511.png]]
### advantages of perfect sized arrays
- methods that use perfect size arrays have fewer parameters than methods that use oversize arrays.
- a perfect size array contains no excess elements
Disadvantage: if the number of array elements needs to change, a new array will have to be constructed.

## 10.19 using references in methods
==Arrays can be used in methods just like int and double values. However, an array is stored in memory differently than variables of primitive data types, like int or double. An int and double variable is stored directly in the stack frame. An array is stored indirectly in the heap, and only the reference to the array is stored in the stack frame. This subtle difference in storage means that arrays behave differently in methods than int and double variables.==
- common error: trying to modify an array reference in a method.

## 10.20 returning arrays from methods
- Methods often need to modify an array's size, but an array's length cannot be modified. Instead a new array with the modified size must be constructed.
	- If a method needs to modify an array's size
		- the method must construct a new array with the new size,
		- copy the existing array's elements to the new array
		- The original array reference must be assigned with the reference to the new array returned by the method

## 10.21 Common errors
- Errors made in method signatures are hard to find because programmers forget to look for those errors
	1.  Calculates a value based on the array, leave the array unchanged. If a method does not change the array contents, then the method must be calculating some other value that must be returned. Ex: The Arrays class' method `int binarySearch(int[] arrayReference, int target)` determines whether target exists in the array data. The returned value is the index of target in the array, or a negative number if target is not in the array.
	2. Changes an array's contents, but not the array's size. If a method changes the array's contents, the method usually has a void return type. Ex: The Arrays class' method `void sort(int[] arrayReference)` changes the array contents to be in ascending order.
	3. Creates a new array or changes the array's size (and possibly contents). Since array references cannot be changed inside a method, a method that returns a newly constructed array must return an array reference. Ex: The Arrays class' method `double[] copyOf(double[] arrayReference, int newLength)` creates a copy of the arrayReference with the length newLength.
	4. ![[Pasted image 20251110190447.png]]
- 
- 
- An error that unintentionally modifies data is known as a side effect
	- A common side effect is a method that calculates values based on an array, but unintentionally modifies the array. Methods should perform exactly one task. A method can calculate something or change the array contents, but should not do both
	- -Use a different algorithm that does not require sorting the array.
	- Make a copy of the array and perform the calculation using the copy.

## 10.22 searching and algorithms
- Linear search is a search algorithm that starts from the beginning of a list, and checks each element until the search key is found or the end of the list is reached.
- An algorithm's **runtime** is the time the algorithm takes to execute.
	- ==If each comparison takes 1 µs (1 microsecond), a linear search algorithm's runtime is up to 1 s to search a list with 1,000,000 elements, 10 s for 10,000,000 elements, and so on. Ex: Searching Amazon's online store, which has more than 200 million items, could require more than 3 minutes.==
	
## 10.23 Binary search
