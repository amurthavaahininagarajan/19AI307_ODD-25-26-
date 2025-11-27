# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 

## AIM:
To check whether a given number is a prime number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user.
4.	If the number is less than or equal to 1, mark it as not prime.
5.	Otherwise, check divisibility from 2 to the square root of the number.
6.	If any divisor is found, mark the number as not prime; otherwise, it is prime.
7.Print whether the number is prime or not.	





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.*;

public class PrimeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer num = sc.nextInt();
        boolean isPrime = true;

        if (num <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime)
            System.out.println(num + " is a prime number.");
        else
            System.out.println(num + " is not a prime number.");
    }
}
```






## OUTPUT:
<img width="699" height="270" alt="image" src="https://github.com/user-attachments/assets/0b758dbf-ae82-48e6-9a45-db21c9f98766" />



## RESULT:
The program successfully determines and displays whether the given number is a prime number.
