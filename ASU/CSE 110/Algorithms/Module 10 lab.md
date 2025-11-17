```
import java.io.IOException;
import java.io.FileInputStream;
import java.util.ArrayList;
import java.util.Scanner;
import java.io.FileOutputStream;
import java.io.PrintWriter;

class Main {
//The commented out below is my test script.  The assignment script is uncommented below.

// public static void main(String[] args) throws IOException {
// ArrayList<Double> list = new ArrayList<Double>();
// ArrayList<Double> list2 = new ArrayList<Double>();
// list.add(2.0);
// list.add(1.0);
// list.add(3.0);
// list.add(5.0);
// list.add(4.0);
// list2.add(2.0);
// list2.add(1.0);
// list2.add(3.0);
// list2.add(5.0);
// list2.add(4.0);

// double avg = getAverage(list);
// double min = getMin(list);
// double max = getMax(list);
// System.out.println("getAverage out: " + avg);
// System.out.println("getMin out: " + min);
// System.out.println("getMax out: " + max);
// center(list);
// System.out.println("center out: " + list);
// scale(list,100.0);
// System.out.println("scale out: " + list);
// normalize(list2);
// System.out.println("normalize out: " + list2);
// System.out.println("loadData out: " + loadData("data1.dat"));
// saveData(list2);
// }

public static void main(String[] args) throws IOException {
Scanner scnr = new Scanner(System.in);
ArrayList<Double> myData = null;
// Collect data file name from user
System.out.print("Enter data file name : ");
String dataFileName = scnr.nextLine();
// get the data from the file
myData = loadData(dataFileName);
// normalize the data
normalize(myData);
// outut the normalized data to the required file
saveData(myData);
}

🚩methods start here 🚩
public static double getAverage(ArrayList<Double> data){
double sum = 0.0;
for(double val : data){
sum += val;
}
return sum/data.size();
}
  

public static double getMin(ArrayList<Double> data){
double min = data.get(0);
for(int i=0; i<data.size(); i++){
if(data.get(i) < min){
min = data.get(i);
}
}
return(min);
}

public static double getMax(ArrayList<Double> data){
double max = data.get(0);
for(int i=0; i<data.size(); i++){
if(data.get(i) > max){
max = data.get(i);
}
}
return(max);
}

public static void center(ArrayList<Double> data){
double avg = getAverage(data);
for(int i=0; i<data.size(); i++){
data.set(i, data.get(i)-avg);
}
}

public static void scale(ArrayList<Double> data, double range){
double currRange = getMax(data) - getMin(data);
double factor = range / currRange;
for(int i=0; i<data.size(); i++){
data.set(i, data.get(i) * factor);
}
}

public static void normalize(ArrayList<Double> data){
center(data);
scale(data,100);

}

public static ArrayList<Double> loadData(String filename)throws IOException{
ArrayList<Double> data = new ArrayList<Double>();
FileInputStream myFile = new FileInputStream(filename);
Scanner myFileReader = new Scanner(myFile);

while(myFileReader.hasNextDouble()){
double value = myFileReader.nextDouble();
data.add(value);
}

myFileReader.close();
myFile.close();
return data;

}

public static void saveData(ArrayList<Double> data)throws IOException{
FileOutputStream myfile = new FileOutputStream("normal.dat");
PrintWriter MyFileWriter = new PrintWriter(myfile);
for(double val:data){
MyFileWriter.printf("%.2f\n", val);
}

MyFileWriter.close();
myfile.close();
}

}
```

## individual Ex p1
```
import java.util.ArrayList;
public class Main {
public static void main(String[] args) {
ArrayList<Integer> arr = new ArrayList<Integer>();
arr.add(1);
arr.add(22);
arr.add(333);
arr.add(400);
arr.add(5005);
arr.add(9);
printArrayList(arr, " _ ");

}

public static void printArrayList(ArrayList<Integer> arr, String sep){
for(int i=0;i<arr.size();i++){
if(i != arr.size() - 1){
System.out.print(arr.get(i) + sep);
} else {
System.out.print(arr.get(i));
}
}
}
}
```