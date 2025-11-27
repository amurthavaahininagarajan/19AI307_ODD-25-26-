# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
```
Lovely found a magic machine that tells her how two numbers relate to each other.
The machine supports all 6 relational operators:

Operator	Meaning
==	Is equal to
!=	Is not equal to
>	Greater than
<	Less than
>=	Greater than or equal to
<=	Less than or equal to
Lovely enters two numbers. The machine prints the result (true or false) for each operator.

Input Format
First line: First integer number (a)

Second line: Second integer number (b)

Output Format
Print:

a == b: <true/false>
a != b: <true/false>
a > b: <true/false>
a < b: <true/false>
a >= b: <true/false>
a <= b: <true/false>
```

## AIM:
To check whether all logical conditions based on two numbers are satisfied and determine if the gate opens.

## ALGORITHM :
1.Start the program and read two integers from the user.
2.Calculate the sum of the two numbers and check whether the sum is greater than 50.
3.Find the absolute difference between the numbers and check if it is less than 30.
4.Compute the product of the two numbers and verify whether the product is even.
5.Check that both numbers are not the same; if all conditions are satisfied, display “Gate Opens”, otherwise display “Gate Does Not Open”.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber: 212222240008
*/
```

## Sourcecode.java:
```
import java.util.*;
public class Main{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println("a == b: "+(a==b));
        System.out.println("a != b: "+(a!=b));
        System.out.println("a > b: "+(a>b));
        System.out.println("a < b: "+(a<b));
        System.out.println("a >= b: "+(a>=b));
        System.out.println("a <= b: "+(a<=b));
    }
    
}
```

## OUTPUT:

<img width="863" height="366" alt="image" src="https://github.com/user-attachments/assets/cfe211e5-fe51-49f2-8843-eac1ba64fbe6" />

## RESULT:
The program correctly compares the two input integers and displays all the relational operator results between them.
