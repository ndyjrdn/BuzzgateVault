```
public class BubbleSortExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      print(myArray);
 
      sort(myArray);
 
      print(myArray);
   }
 
   public static void sort(double[] values) {
      boolean isSorted = false;
 
      while (! isSorted) {
         isSorted = true;
         int index = 1;
 
         while (index < values.length) {
            if (values[index] < values[index - 1]) {
               swapByIndex(index, index - 1, values);
               isSorted = false;
            }
            index += 1;
         }
      }
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