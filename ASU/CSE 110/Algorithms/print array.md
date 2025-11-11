```
public class ArrayPrinterExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      print(myArray);
   }
 
   public static void print(double[] values) {
      for (double value : values)
         System.out.print(value + " - ");
 
         System.out.println();
   }
}
```