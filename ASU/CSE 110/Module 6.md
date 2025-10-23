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
- A method can return