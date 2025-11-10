```
public class FindFirstExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0, 2.5};
 
      int foundIndex = findFirst(myArray, 2.5);
      System.out.println("2.5 is first found at index : " + foundIndex);
 
      foundIndex = findFirst(myArray, 9.9);
      System.out.println("9.9 is first found at index : " + foundIndex);
   }
 
   public static int findFirst(double[] values, double target) {
      for (int index = 0; index < values.length; index++)
         if (values[index] == target)
            return index;
 
      return -1;
   }
}

```