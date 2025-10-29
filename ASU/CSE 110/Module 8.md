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

