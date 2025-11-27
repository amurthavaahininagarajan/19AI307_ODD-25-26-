# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
```
Assign exam room based on:

Gender and subject code

Male taking subject 1 or 2 → print("A")

Female taking subject 1 → print("B")

Female taking subject 2 → print("C")

All others → print("Admin")

Except above any input should print ("Invalid")
Write a java program that gets input from user for gender and subject, allot room based above conditions.
```
## AIM:
To write a program that reads the gender and subject code of a student and displays the correct exam room based on the given conditions.

## ALGORITHM :
1.Start the program and read the student’s gender and subject code as input.
2.Check if the gender is male (m):
  *If subject is 1 or 2, assign room A.
  *If subject is between 1 and 5, display Admin.
  *Otherwise, display Invalid.
3.Check if the gender is female (f):
  *If subject is 1, assign room B.
  *If subject is 2, assign room C.
  *If subject is between 1 and 5, display Admin.
  *Otherwise, display Invalid.
4.If the gender is neither ‘m’ nor ‘f’, print Invalid.
5.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber: 212222240008
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ExamRoom {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String gender = sc.next();
        int subject = sc.nextInt();

        if (gender.equalsIgnoreCase("m")) {
            if (subject == 1 || subject == 2) System.out.println("A");
            else if (subject >= 1 && subject <= 5) System.out.println("Admin");
            else System.out.println("Invalid");
        } else if (gender.equalsIgnoreCase("f")) {
            if (subject == 1) System.out.println("B");
            else if (subject == 2) System.out.println("C");
            else if (subject >= 1 && subject <= 5) System.out.println("Admin");
            else System.out.println("Invalid");
        } else {
            System.out.println("Invalid");
        }
    }
}
```





## OUTPUT:

<img width="522" height="337" alt="image" src="https://github.com/user-attachments/assets/c97832b2-7035-4129-9494-736e31551c35" />


## RESULT:
The program successfully reads gender and subject code, checks all the given conditions, and correctly displays the appropriate exam room or an invalid message.
