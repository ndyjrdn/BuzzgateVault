```
public class MinValueExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      double min = minimum(myArray);
      System.out.println("Minimum is : " + min);
   }
 
   public static double minimum(double[] values) {
      double min = values[0];
 
      for (double value : values)
         if (value < min)
            min = value;
 
      return min;
   }
}

```