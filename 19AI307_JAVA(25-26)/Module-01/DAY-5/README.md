# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to find the absolute value of a number using Math.abs().

## AIM:
To read a number and print its absolute value.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user.
4.Compute its absolute value using Math.abs().
5.Display the absolute value.
```

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber: 212222240008
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class Value{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        double num=sc.nextDouble();
        double absValue=Math.abs(num);
        System.out.println("Absolute value = "+absValue);
        sc.close();
    }
}
```





## OUTPUT:

<img width="647" height="334" alt="image" src="https://github.com/user-attachments/assets/ad456c37-bd29-4fcf-982c-13fd2961fb45" />


## RESULT:
The program successfully reads a number, computes its absolute value, and prints it.

