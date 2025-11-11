```
public class MaxValueExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      double max = maximum(myArray);
      System.out.println("Maximum is : " + max);
   }
 
   public static double maximum(double[] values) {
      double max = values[0];
 
      for (double value : values)
         if (value > max)
            max = value;

      return max;
   }
}

```