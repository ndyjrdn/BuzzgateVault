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
