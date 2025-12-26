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
