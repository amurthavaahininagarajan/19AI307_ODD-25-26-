# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to print all elements in an array that are greater than a given value

## AIM:
To read an array and print all elements greater than a given value.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the size of the array n.
4.Read n elements into the array.
5.Read the comparison value.
6.Traverse the array and print each element that is greater than the given value.
7.If no such element exists, print “No elements greater than value”.
```
## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber: 212222240008
*/
```

## SOURCE CODE:
```
import java.util.*;
public class GreaterThanValue {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int arr[] = new int[n];
        
        for(int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        
        int value = sc.nextInt();
        boolean found = false;
        
        for(int i = 0; i < n; i++) {
            if(arr[i] > value) {
                System.out.println(arr[i]);
                found = true;
            }
        }
        
        if(!found)
            System.out.println("No elements greater than " + value);
    }
}
```






## OUTPUT:
<img width="784" height="699" alt="image" src="https://github.com/user-attachments/assets/6efd40ef-6bcc-460c-bfa8-81d174894f97" />



## RESULT:
The program successfully checks the array and prints all elements greater than the given value or displays a message if none are found.

