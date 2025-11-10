```
public class SwapExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      print(myArray);
 
      swapByIndex(0, 4, myArray);
 
      print(myArray);
   }
 
   public static void swapByIndex(int index1, int index2, double[] values) {
      double temp = values[index1];
      values[index1] = values[index2];
      values[index2] = temp;
   }
 
   public static void print(double[] values) {
      for (double value : values)
         System.out.print(value + " - ");
 
         System.out.println();
   }
}

```