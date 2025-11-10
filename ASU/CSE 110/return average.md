```
public class AverageExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      double avg = average(myArray);
      System.out.println("Average is : " + avg);
   }
 
   public static double average(double[] values) {
      double sum = sum(values);
      double average = sum / values.length;

      return average;
   }
    
   public static double sum(double[] values) {
      double sum = 0.0;
 
      for (double value : values)
         sum += value;
 
      return sum;
   }
}
```