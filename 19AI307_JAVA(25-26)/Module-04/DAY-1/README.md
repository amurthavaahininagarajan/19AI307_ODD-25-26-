# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?


## AIM:

To read a string and check whether it is “null” or convert it to uppercase.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string input from the user.
4.	Trim the input to remove extra spaces.
5.	If the input equals “null” (case-insensitive), print “Null element”.
6.	Otherwise, convert the input to uppercase and print it.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        
        String input = sc.nextLine().trim();
        
       
        if (input.equalsIgnoreCase("null")) {
            System.out.println("Null element");
        } else {
            
            System.out.println(input.toUpperCase());
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="593" height="271" alt="image" src="https://github.com/user-attachments/assets/da2b2b25-8a46-4e97-b1c8-7baa3fc66cd8" />


## RESULT:
The program successfully identifies a null-like input or converts the given string to uppercase.
