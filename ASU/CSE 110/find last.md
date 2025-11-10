```
public class FindLastExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0, 2.5};
 
      int foundIndex = findLast(myArray, 2.5);
      System.out.println("2.5 is last found at index : " + foundIndex);
 
      foundIndex = findLast(myArray, 9.9);
      System.out.println("9.9 is last found at index : " + foundIndex);
   }
 
   public static int findLast(double[] values, double target) {
      for (int index = values.length - 1; index >= 0; index--)
         if (values[index] == target)
            return index;
 
      return -1;
   }
}
```