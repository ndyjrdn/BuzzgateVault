## 14.1 Choosing classes to create
- ### Decomposing into classes

Creating a program may start by a programmer deciding what "things" exist, and what each thing contains and does.
https://learn.zybooks.com/zybook/2025FallB-X-CSE110-63951/chapter/14/section/1
 ## 14.2 Classes and ArrayLists
 ### ArrayList of objects: A reviews program

A programmer commonly uses classes and ArrayLists together.

### A class with an ArrayList: The Reviews class

A class can also involve ArrayLists.  creating a Reviews class for managing an ArrayList of Review objects.


      currRating = scnr.nextInt();
## 14.3 ArrayList ADT
- review of .get .add .remove etc from ArrayList

## 14.4 Parameters or reference types
for reference variables if the var1=var2 sets them to the same reference rather than duplicating so this doesn't create a new object.  Just multiple references to the same object

**THIS**

![[Pasted image 20251121130350.png]]

## 14.5 Static fields and methods
- instance members are object specfic
- Static members are shared by all objects of a class
	- Data or methods
- Static method like Math.sqrt() - don't have to declare a Math object
- 
![[Pasted image 20251121131744.png]]

## 14.6 Mechanics of classes
An object and the variable that refers to it are two different things.

Life cycle of a Bunny Object:
```java
class Bunny {
 public String name = "";

     public int age = 0;



     public Bunny() {

         // a default constructor that does nothing

     }


     public Bunny(String name, int age) {

         this.name = name;

         this.age = age;

     }



     public void hop() {

         System.out.print(this.age + " year old " + this.name);

         System.out.println(" hops around.");

    }

 }



 public class Main {

     public static void main(String []args) {

         Bunny flopsy = new Bunny("Flopsy", 8);

         flopsy.hop();

     }

 }
```