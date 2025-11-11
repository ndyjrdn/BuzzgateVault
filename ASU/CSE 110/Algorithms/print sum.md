```
public class SumPrinterExample{
   
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      printSum(myArray);
   }
 
   public static void printSum(double[] values) {
      double sum = 0.0;
 
      for (double value : values)
         sum += value;
 
         System.out.println(sum);
   }
}

```