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
## output:




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

## output




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
# output




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

# output

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
# output

![output](Experiment-2/EXPERIMENT-2(C).png)



# ADDITIONALEXPERIMENTS

## AdditionalExperiment-1
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
# output
![output]()

