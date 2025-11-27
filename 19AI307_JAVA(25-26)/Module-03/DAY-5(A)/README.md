# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To check whether a given number is an Armstrong number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user.
4.	Count the number of digits in the number.
5.	Extract each digit and raise it to the power of the total number of digits.
6.	Add all powered digits to form a sum.
7.	Compare the sum with the original number and print whether it is an Armstrong number or not.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int temp = num;
        int digits = Integer.toString(num).length();
        int sum = 0;

        while (temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }

        if (sum == num)
            System.out.println(num + " is an Armstrong number.");
        else
            System.out.println(num + " is not an Armstrong number.");
    }
}

```






## OUTPUT:

<img width="829" height="270" alt="image" src="https://github.com/user-attachments/assets/3e461f47-4703-4be6-bc17-09254505ceb6" />


## RESULT:
The program correctly checks and displays whether the given number is an Armstrong number.
