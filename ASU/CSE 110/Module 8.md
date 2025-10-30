## 8.1 If-else branches

### Flowcharts
![[Pasted image 20251029103940.png]]
Decision (if-else)
![[Pasted image 20251029104050.png]]
Repetition (loops)
![[Pasted image 20251029104126.png]]

- ==Every program ever written is composed of just these 3 structures==
- We can stack them
- Nest them
- Replace them
### Stacking 
![[Pasted image 20251029104451.png]]

### Nesting
![[Pasted image 20251029104525.png]]

### Replacing
![[Pasted image 20251029104637.png]]

- in a program a branch is a sequence only executed under certain condition
- An if-else can be extended to an if-elseif-else structure. Each branch's expression is checked in sequence; as soon as one branch's expression is found to be true, that branch is taken. If no expression is found true, execution will reach the else branch, which then executes.
-
## Detecting equal values with branches
- a single selection decision is when basically a yes/no to run instructions or not.
- If false, no else is provided and the inst. is skipped
- ![[Pasted image 20251029144215.png]]
- {} braces
- [] brackets

 - can have multiple branches 
```
 if(foo == bar){
  do a thing
 } 
 else if(foo == bar2) {
  do another thing
 }
 else {do that other thing}
```

- use relational and equality operatoirs iwth integer, character or floating points
- Should not use equality with floating point though as precision can mess with results
- Strings will cause issues too.

## 8.3 multi selection decisions
if/else if / else if / yada / else

## 8.4 Detecting ranges with branches
- relational operators are also called comparison operators
- ALWAYS boolean

## 8.5 Detecting ranges using logical operators
[[Logical Operators]]

## Detecting rages with gaps
- If the range isn't in the gap.  
- ie
```
	if(age < 21){
	   output this
	} 
	else if(age > 50){
		output this
	}
	else{ The gap is 21 to 50}
```

Can join operators like![[Pasted image 20251029165226.png]]

## 8.7 Detecting multiple features with branches
- This is just a sequence of if statements.  Each is evaluated and executed independently

##  8.8 Common branching errors

- With one statement branches the braces are strictly necessary but use them for readability 
- Using = instead of ==


##  8.9 Example
##  8.10 order of operations
[[Operator Precedence Rules]]
- A common error often made by new programmers is to write expressions like `(16 < age < 25)`, as one might see in mathematics.
- The meaning however almost certainly is not what the programmer intended. The expression is evaluated left-to-right, so evaluation of `16 < age` yields true. Next, the expression `true < 25` is evaluated. This expression attempts to compare a Boolean value true to an integer value 25, which is not allowed in Java. The Java compiler will report a compilation error similar to: "operator < cannot be applied to boolean,int".

## 8.11 Switch statements
==Remember that Java's `switch` statement is limited and cannot do everything that an else-if ladder can do. Java's `switch` statement only works with the following Java primitive data types: `byte`, `short`, `char`, and `int`. It also works with Java's `String` type.==
A switch statement can more clearly represent multi-branch behavior involving a variable being compared to constant values. The program executes the first case whose constant expression matches the value of the switch expression, executes that case's statements, and then jumps to the end. If no case matches, then the default case statements are executed.
- only int, char, string.
- order agnostic
- Case can't be a variable
- Without a break statement in the case of a switch, the remaining statements will execute.

## 8.12 Boolean data type
- booleans can be set with expressions
	-  Ex: `isLargeParty = (partySize > 6);` assigns isLargeParty with the result of the expression partySize > 6.

#  8.13 String comparisons
- str1.equals(str2) evaluates for exact match.  like == in numbers.
- When comparing greater than/less than Capitals come first alphabetically,.
- Shorter words come first
- 
[[String methods]]
