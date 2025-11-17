```java
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
```java
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
## p2
```java
import java.util.ArrayList;
public class Main {
public static void main(String[] args) {
ArrayList<Integer> arr = new ArrayList<Integer>();
arr.add(1);
arr.add(2);
arr.add(1);
arr.add(3);
arr.add(2);
arr.add(5);
arr.add(6);
arr.add(2);
arr.add(4);
System.out.println(count(arr, 2));

}
public static int count(ArrayList<Integer> arr, int num){
int count = 0;
for(int val : arr){
if(val == num){
count++;
}
}
return count;
}
}
```

## p3
```java
import java.util.ArrayList;
public class Main {
public static void main(String[] args) {
ArrayList<Integer> arr = new ArrayList<Integer>();
arr.add(1);
arr.add(2);
arr.add(1);
arr.add(3);
arr.add(2);
arr.add(5);
arr.add(6);
arr.add(2);
arr.add(4);
System.out.println(countInRange(arr,1,6));
}

public static int countInRange(ArrayList<Integer> arr, int num1, int num2){
int count = 0;
for(int val : arr){
if(val >= num1 && val <= num2)
count++;
}
return(count);
}
}
```

## P4
```java
import java.util.ArrayList;
public class Main {
public static void main(String[] args) {
ArrayList<Integer> arr = new ArrayList<Integer>();
arr.add(3);
arr.add(2);
arr.add(7);
arr.add(5);
arr.add(8);
arr.add(6);
System.out.println(getAllOdd(arr));
}

public static ArrayList<Integer> getAllOdd(ArrayList<Integer> arr){
ArrayList<Integer> newArr = new ArrayList<Integer>();
for(int val : arr){
if(val % 2 == 1){
newArr.add(val);
}
}
return newArr;
}
}
```

## p5 remove duplicates
```java
import java.util.ArrayList;

public class Main {
public static void main(String[] args) {
ArrayList<Integer> arr = new ArrayList<Integer>();
arr.add(1);
arr.add(1);
arr.add(2);
arr.add(2);
arr.add(3);
arr.add(3);
arr.add(4);
System.out.print(noDuplicates(arr));
}

public static boolean contains(ArrayList<Integer> list, int num){
for(int i : list){
if(i == num){
return true;
}
}
return false;
}

public static ArrayList<Integer> noDuplicates(ArrayList<Integer> list){
ArrayList<Integer> result = new ArrayList<Integer>();
for(int i : list){
if(!contains(result, i)){
result.add(i);
}
}
return(result);
}
}
```

## p6
``` java
import java.util.ArrayList;
public class Main {
public static void main(String[] args) {
ArrayList<Integer> list1 = new ArrayList<Integer>();
list1.add(1);
list1.add(2);
list1.add(1);
list1.add(3);
list1.add(2);
list1.add(5);
list1.add(5);
list1.add(2);
list1.add(4);
ArrayList<Integer> list2 = new ArrayList<Integer>();
list2.add(1);
list2.add(2);
list2.add(3);

System.out.println(countInList(list1, list2));

}
public static int countInList(ArrayList<Integer> list1, ArrayList<Integer> list2){
int count = 0;
for(int i:list2){
for(int j:list1){
if(i==j){
count++;
}
}
}
return count;
}
}
```

## P8
```java
// This program should ask the user for the name of the file that they would like to display.

// The program will then open the file with the user specified name,

// and display the contents of that file to the console.

//

// You must fill in the two missing pieces described in the code below.

// 1. you must write the getFileName method.

// 2. You must call the displayFileContents method from within the main method.

//

// make no other changes to the code, and make no changes to any of the provided .txt files.

  

import java.util.Scanner;
import java.io.FileInputStream;
import java.io.IOException;

class Main {
// use the scnr Scanner variable defined below to collect any user input

public static Scanner scnr = new Scanner(System.in);
public static void main(String[] args) throws IOException {
String fileName = getFileName();

/* 2) Call the displayFileContents method and pass the fileName as an argument */
displayFileContents(fileName);
}

public static String getFileName(){
System.out.print("enter filename: ");
String filename = scnr.next();
return filename;

}

/* 1) Write a public static method named getFileName.

This method should take no arguments.

This method should prompt the user to enter a complete file name.

This method should collect the user's input in a String variable.

This method should return the value stored in the String variable. */

  
  

// Make no changes to the displayFileContents method below

public static void displayFileContents(String fileName) throws IOException {
// declare a FileInputStream variable
// and instantiate a FileInputStream object for the file with the given FileName
FileInputStream myFile = new FileInputStream(fileName);
// declare a Scanner variable
// and instantiate a Scanner object attached to the File
Scanner myFileReader = new Scanner(myFile);
// loop while the Scanner has a next line
while (myFileReader.hasNextLine()) {
// read the next line from the Scanner and store it in a String variable
String line = myFileReader.nextLine();
// print the String to the console
System.out.println(line);

}
}
}
```

## p10
```java
// This program should ask the user for the name of the file that they would like to open.
// The program will then open the file with the user specified name,
// and total up the list of integers in the file.
// Input files will always have one integer on each line.
// There may be a different number of lines in each input file.
// You must fill in the missing piece described in the code below.
// 1) you must write the sumFileContents method.
  
// make no other changes to the code,
// and make no changes to any of the provided .dat files.
  

import java.util.Scanner;
import java.io.FileInputStream;
import java.io.IOException;

class Main {
// The scnr Scanner variable defined below will be used to collect any user input
public static Scanner scnr = new Scanner(System.in);
public static void main(String[] args) throws IOException {
String fileName = getFileName();
int sum = sumFileContents(fileName);
System.out.println("The sum is: " + sum);
}

public static String getFileName() {
System.out.print("Enter file name: ");
return scnr.nextLine();

}

/* 1) Write a public static method named sumFileContents.

This method should take one String argument (a complete file name).

This method should open the specified file.

This method should read in all of the integers in the file and add each to a total.

This method should return an int (the total of all integers in the file).

Be sure to add the 'throws IOException' clause after the parameter list.*/

public static int sumFileContents(String fileName) throws IOException{
FileInputStream myFile = new FileInputStream(fileName);
Scanner myFileReader = new Scanner(myFile);
int result = 0;
while(myFileReader.hasNextInt()){
result += myFileReader.nextInt();
}
return result;

  

}

  

}
```

## p11
```java
// This program will copy the contents of one file into another file,
// line by line.
// You must complete the `makeCopy` method and fill in the missing pieces described in the code below.
// 1) you must write a loop to iterate while the scanner has a next line.
// within the loop you must ...
// 2) use the scanner to read the next line from the input file and store it in a String variable.
// 3) use the file writer to write the String to the output file.
// after the loop you must ...
// 4) flush the PrintWriter
// 5) close the PrintWriter
// make no other changes to the code,

  
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.PrintWriter ;
import java.io.IOException;
import java.util.Scanner;

class Main {
public static void main(String[] args) throws IOException {
makeCopy("original.dat", "copy.dat");
// print out the contents of the copy to
// verify that the original was copied correctly

printFile("copy.dat");
}

public static void makeCopy(String inputFileName, String outputFileName) throws IOException {
// open a File with the given inputFileName
// and instantiate a Scanner object to read the File
Scanner myFileReader = new Scanner(new FileInputStream(inputFileName));
// open a File with the given outputFileName
// and instantiate a PrintWriter object to write to the File
PrintWriter myFileWriter = new PrintWriter(new FileOutputStream(outputFileName));
while(myFileReader.hasNextLine()){
// 1) loop while the Scanner has a next line
// 2) read the next line from the Scanner and store it in a String variable
String var = myFileReader.nextLine();
// 3) write the line to the output file
myFileWriter.println(var);
// loop ends
}
// 4) flush the PrintWriter
myFileWriter.flush();
// 5) close the PrintWriter
myFileWriter.close();
myFileReader.close();
}
// make no changes to this printFile method
public static void printFile(String fileName) throws IOException {

Scanner myFileReader = new Scanner(new FileInputStream(fileName));

while (myFileReader.hasNextLine()) {

System.out.println(myFileReader.nextLine());

}

myFileReader.close();

}
}
```

## p 12
```java

```