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
- 