# JAVALAB
## 1a:
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






## 1b
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


