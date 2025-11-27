# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To compute the cube of a number using a square method inside a class.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a method square(x) to return x*x.
4.Define a method cube(x) to return x*square(x).
5.Read an integer from the user.
6.Create an object of the CubeUsingSquare class.
7.Call the cube method and display the result.
```




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class CubeUsingSquare {
    int square(int x) {
        return x * x;
    }

    int cube(int x) {
        return x * square(x);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        CubeUsingSquare obj = new CubeUsingSquare();
        System.out.println(obj.cube(x));
        sc.close();
    }
}
```





## OUTPUT:
<img width="563" height="258" alt="image" src="https://github.com/user-attachments/assets/6a267a44-c9ef-463e-9eee-708139ba7a22" />



## RESULT:
The program successfully calculates the cube of the given number using the square method.

