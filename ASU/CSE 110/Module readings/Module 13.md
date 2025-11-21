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
      while (currRating >= 0) {
         currReview = new Review();
         currComment = scnr.nextLine(); // Gets rest of line
         currReview.setRatingAndComment(currRating, currComment);
         reviewList.add(currReview);
         currRating = scnr.nextInt();
      }
   }