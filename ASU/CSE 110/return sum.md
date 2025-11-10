```
	public class SumExample{
 
   public static void main(String[] args) {
      double[] myArray = {3.14, 1.1, 2.5, 6.81, 5.0};
 
      double total = sum(myArray);
      System.out.println("Total is : " + total);
   }
 
   public static double sum(double[] values) {
      double sum = 0.0;
 
      for (double value : values)
         sum += value;
 
      return sum;
   }
}


```