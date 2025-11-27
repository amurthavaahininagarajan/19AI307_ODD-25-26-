# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
```
A perfect number is a positive integer that is equal to the sum of its proper divisors (excluding itself). For example:

6 is a perfect number because its divisors 1, 2, 3 sum up to 6.

28 is a perfect number because its divisors 1, 2, 4, 7, 14 sum up to 28.

Write a Java program that:

Prompts the user to enter a positive integer N.

Finds and displays all perfect numbers from 1 up to N.

Uses a loop to check each number for perfection by calculating the sum of its divisors.
```
## AIM:
To find and display all perfect numbers from 1 to the given number N.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the value of N from the user.
4.For each number from 1 to N, initialize sum = 0.
5.Check all divisors of the number up to num/2 and add them to sum.
6.If the sum of divisors equals the number, print the number as a perfect number.
7.If no perfect number is found, print “None”.


## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber: 212222240008 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class PerfectNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int N = sc.nextInt();

        System.out.print("Perfect numbers: ");
        boolean found = false;

        for (int num = 1; num <= N; num++) {
            int sum = 0;
            for (int i = 1; i <= num / 2; i++) {
                if (num % i == 0)
                    sum += i;
            }
            if (sum == num) {
                System.out.print(num + " ");
                found = true;
            }
        }

        if (!found)
            System.out.print("None");
    }
}
```





## OUTPUT:
<img width="705" height="328" alt="image" src="https://github.com/user-attachments/assets/8547d736-ac35-430b-b087-99c66a6b6ad8" />



## RESULT:
The program successfully identifies and displays all perfect numbers up to N.
