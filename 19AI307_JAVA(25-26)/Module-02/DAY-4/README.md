# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program that shows how static and non-static variables behave differently with multiple objects 
## AIM:
To demonstrate the difference between static and non-static variables by creating multiple objects.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a static variable to count objects shared by all instances.
4.Declare a non-static variable to count objects individually per instance.
5.Increment both variables inside the constructor and display their values.
6.Read the number of objects to create from the user.
7.Create the specified number of objects inside a loop to show the difference in counts.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class prog {
    static int staticCount = 0;
    int nonStaticCount = 0;
    public prog() {
        staticCount++;
        nonStaticCount++;
        System.out.println("Static Count (shared): " + staticCount);
        System.out.println("Non-static Count (per object): " + nonStaticCount);
        System.out.println("----------------------------------");
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for (int i = 1; i <= n; i++) {
            System.out.println("Creating object #" + i);
            new prog();
        }
    }
}
```






## OUTPUT:

<img width="859" height="568" alt="image" src="https://github.com/user-attachments/assets/dedcb98f-4450-4890-8702-a25877e0e587" />


## RESULT:
The program correctly demonstrates how static variables are shared across all objects while non-static variables reset for each object.
