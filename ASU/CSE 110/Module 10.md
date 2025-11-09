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

- The accessing index is an expression but is also always an integer.  
