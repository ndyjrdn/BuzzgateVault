## 9.1 Loops

- repetition
- Indefinite loop (unknown number of repititions)
- Definite loop (Known/defined number of reps.)
- a loop is a program that repeatedly executes to loop's statements (loop body) while the expression in true
	- Once the expression is false, the programs proceeds past the loop
	- Each rep is an iteration.
## 9.2 while loops
 - syntax 
```
	while(condition){
		body
	} 
```
- while the condition is true repeat instructions
- stop when false
- 

- infinite loops don't have a way to be false.  Either because  the value update is missing or the expression has the opportunity to skip the falsification.
	- good practice is to include greater than or less than along with equality in a loop expression whenever possible, such as userVal >= 0 rather than userVal != 0.
## 9.3 more while loop examples
- when to use:
	- repetition 
	- need to return to a previous point
- counter pattern:
	- Adding or subtracting the variable as it iterates to reach the falsifying iteration
- sentinel pattern:
	- guard condition that prevents or allows the loop (checks for true) each iteration
	- Loops are commonly used to process an input list of values. A sentinel value is a special value indicating the end of a list, such as a list of positive integers ending with 0, as in 10 1 6 3 0. The example below computes the average of an input list of positive integers, ending with 0. The 0 is not included in the average.
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
