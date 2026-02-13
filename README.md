# JAVALAB
## EXPERIMENT-1
##  Experiment-1(A)
```java
class PrimitiveDataTypes{
byte b;
short s;
int i;
float f;
long l;
double d;
char c;
boolean bool;
public static void main(String args[]){
PrimitiveDataTypes obj = new PrimitiveDataTypes();
System.out.println("Default byte value:"+obj.b);
System.out.println("Default short value:"+obj.s);
System.out.println("Default int value:"+obj.i);
System.out.println("Default float value:"+obj.f);
System.out.println("Default long value:"+obj.l);
System.out.println("Default double value:"+obj.d);
System.out.println("Default charvalue:"+obj.c);
System.out.println("Default boolean value:"+obj.bool);
}
}
```
## OUTPUT:




![output](EXPERIMENTS/Experiment-1(A).png)






## Experiment-1(B)
```java
import java.util.Scanner;
class QuadraticEquations{
public static void main(String args[])
{
Scanner sc = new Scanner(System.in);
double a, b, c, D;
System.out.println("Enter value of a:");
a = sc.nextDouble();
System.out.println("Enter value of b:");
b = sc.nextDouble();
System.out.println("Enter value of c:");
c = sc.nextDouble();
D = b * b - 4 * a * c;
System.out.println("Discriminent"+D);
if (D > 0)
{
double root1 = (-b + (Math.sqrt(D))) / (2 * a);
double root2 = (-b - (Math.sqrt(D))) / (2 * a);
System.out.println("Roots are real and distinct");
System.out.println("Root 1 = " + root1);
System.out.println("Root 2 = " + root2);
}
else if (D == 0)
{
double root = -b / (2 * a);
System.out.println("Roots are real and equal");
System.out.println("Root = " + root);
}
else
{
double real = -b / (2 * a);
double imaginary = Math.sqrt(-D) / (2 * a);
System.out.println("Roots are complex and imaginary");
System.out.println("Root 1 = " + real + " + i" + imaginary);
System.out.println("Root 2 = " + real + " - i" + imaginary);
}
sc.close();
}
}
```

## OUTPUT:




![output](EXPERIMENTS/Experiment-1(B).png)




# EXPERIMENT-2
## Experiment-2(A)
```java

class MyClass{
void displayMessage(){
System.out.println("Welcome to java lab");
}
int add (int a , int b){
return a+b;
}
public static void main(String args[]){
MyClass obj=new MyClass();
obj.displayMessage();
int result =obj.add(10,20);
System.out.println("Sum"+result);
}
}
```
# OUTPUT:




![output](Experiment-2/EXPERIMENT-2(A).png)



# Experiment-2(B)

```java
class OverloadExample{
int add (int a,int b){
return a+b;
}
double add (double a ,double b)
{
return a+b;
}
int add (int a, int b, int c)
{
return a+b+c;
}
public static void main(String args[]){
OverloadExample obj= new OverloadExample();
System.out.println("Result of adding two integers:"+obj.add(10,20));
System.out.println("Result of adding two double values:"+obj.add(5.5,4.5));
System.out.println("Result of adding three integers values:"+obj.add(1,2,3));
}
}
```

# OUTPUT:

![output](Experiment-2/EXPERIMENT-2(B).png)


# Experiment-2(C)
```java

class Student{
String name;
int age;
int marks;
Student(String n,int a,int m){
name=n;
age=a;
marks=m;
}
void display(){
System.out.println("Name:"+name);
System.out.println("Age:"+age);
System.out.println("Marks:"+marks);
}
public static void main(String args[]){
Student s1=new Student("ALICE",20,85);
s1.display();
}
}
```
# OUTPUT:

![output](Experiment-2/EXPERIMENT-2(C).png)



# ADDITIONALEXPERIMENTS

## AdditionalExperiment-2
```java
import java.util.Scanner;
class Fibonacci{
int n,firstNumber,secondNumber,thirdNumber,sum;
Fibonacci(int number)
{
n=number;
firstNumber=0;
secondNumber=1;
thirdNumber=0;
sum=0;
}
void generate(){
System.out.print("Fibonacci Series: ");
while(n>0){
sum+=firstNumber;
if(n==1)
System.out.print(firstNumber+".");
else
System.out.print(firstNumber+", ");
thirdNumber=firstNumber+secondNumber;
firstNumber=secondNumber;
secondNumber=thirdNumber;
n--;
}
System.out.println("\nSum of Fibonacci series: "+sum);
}
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
System.out.print("Enter the value of n: ");
int number=sc.nextInt();
Fibonacci f=new Fibonacci(number);
f.generate();
}
}
```
# OUTPUT:


![output](AdditionalExperiments/AdditionalExperiment-2.png)









## EXPERIMENT-3
##  Experiment-3(A)
```java

class Student {
    String name;
    int age;
    int marks;

  
    Student() {
        name = "Not Assigned";
        age = 0;
        marks = 0;
    }
    Student(String n, int a) {
        name = n;
        age = a;
        marks = 0;
    }

  
    Student(String n, int a, int m) {
        name = n;
        age = a;
        marks = m;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
        System.out.println();
    }
    public static void main(String[] args) {
        Student s1 = new Student();                
        Student s2 = new Student("Alice", 20);     
        Student s3 = new Student("Bob", 22, 90);   

        s1.display();
        s2.display();
        s3.display();
    }
}
```

# OUTPUT


![output](Experiment-3/Experimetn-3(A).png)





## EXPERIMENT-3
##  Experiment-3(B)
### BinarySearch Class
```java
import java.util.Scanner;

class BinarySearch {
    int[] arr;
    int n;

    BinarySearch(int size) {
        n = size;
        arr = new int[n];
    }

    void setList() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }


        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - 1 - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }

    void getList() {
        System.out.print("Elements in ascending order: ");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    int binarySearch(int key) {
        int low = 0, high = n - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (arr[mid] == key)
                return mid;
            else if (arr[mid] < key)
                low = mid + 1;
            else
                high = mid - 1;
        }
        return -1;
    }
}
```


### MainClass
```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int size = sc.nextInt();

        BinarySearch bs = new BinarySearch(size);

        bs.setList();
        bs.getList();

        System.out.print("Enter the element to search: ");
        int key = sc.nextInt();

        int index = bs.binarySearch(key);

        if (index == -1)
            System.out.println("Element not found");
        else
            System.out.println("Element found at index: " + index);
    }
}
```



![output](Experiment-3/Experiment-3(B).png)






## EXPERIMENT-3
##  Experiment-3(C)
```java
import java.util.Scanner;

class BubbleSortExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];


        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {

                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        System.out.println("Sorted Array in Ascending Order:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }

        sc.close();
    }
}
```





![output](Experiment-3/Experiment-3(C).png)





# ADDITIONALEXPERIMENTS

## AdditionalExperiment-1

```java
import java.util.Scanner;

class Substring {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the main string: ");
        String mainString = sc.nextLine();

        System.out.print("Enter the substring to insert: ");
        String subString = sc.nextLine();

        System.out.print("Enter the position: ");
        int position = sc.nextInt();

        if (position >= 0 && position <= mainString.length()) {
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            String resultString = firstPart + subString + secondPart;
            System.out.println("Resulting string: " + resultString);
        } else {
            System.out.println("Invalid position");
        }
    }
}
```




![output](AdditionalExperiments/AdditionalExperiment-1.png)




# ADDITIONALEXPERIMENTS

## AdditionalExperiment-3

```java

import java.util.Scanner;

class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a String:");
        String str= sc.nextLine();
        int start = 0;
        int end = str.length() - 1;
        while (start < end) {
            if (str.charAt(start) != str.charAt(end)) {
                System.out.println(str+" is not a palindrome");
                return;
            }

            start++;
            end--;
        }
        System.out.println(str+" is a palindrome");
    }
}
```




![output](AdditionalExperiments/AdditionalExperiment-3.png)




# ADDITIONALEXPERIMENTS

## AdditionalExperiment-4

```java
import java.util.Scanner;

public class PerfectNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        int sum = 0;

        for (int i = 1; i < num; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }

        if (sum == num) {
            System.out.println(num + " is a perfect number.");
        } else {
            System.out.println(num + " is not a perfect number.");
        }

        sc.close();
    }
}
```





![output](AdditionalExperiments/AddtionalExperiment-4.png)





## EXPERIMENT-4
##  Experiment-4(A)
### Person Class

```java
public class Person {
    String name;
    int age;

    
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

   
    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```
### Employee Class
```java
public class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

   
    Employee(String name, int age, double annualSalary, int yearOfJoining, String nationalInsuranceNumber) {
        super(name, age); 
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    
    void displayEmployeeDetails() {
        displayPersonDetails(); 
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("National Insurance Number: " + nationalInsuranceNumber);
    }
}
```
### TestEmployee Class
public class TestEmployee {
    public static void main(String[] args) {

        Employee emp1 = new Employee(
                "Rahul",
                28,
                500000.00,
                2022,
                "NI123456A"
        );

        emp1.displayEmployeeDetails();
    }
}
```


![output](Experiment-4(A).png)


