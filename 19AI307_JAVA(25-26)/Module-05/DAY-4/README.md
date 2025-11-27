# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## AIM:
To create two threads, assign names and priorities, and display their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two thread names from the user.
4.	Create two Thread objects.
5.	Assign the input names to the threads.
6.	Set priorities for both threads.
7.	Print the thread details using the default toString() method.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
public class Main {
    public static void main(String[] args) {
        java.util.Scanner sc = new java.util.Scanner(System.in);

        // Read thread names from user
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        // Create two threads
        Thread t1 = new Thread();
        Thread t2 = new Thread();

        // Set names
        t1.setName(name1);
        t2.setName(name2);

        // Set priorities
        t1.setPriority(4);
        t2.setPriority(2);

        // Print thread details
        System.out.println(t1);
        System.out.println(t2);
    }
}
```





## OUTPUT:
<img width="849" height="299" alt="image" src="https://github.com/user-attachments/assets/923b86b3-1b25-4be1-b3da-24ab93cf0e91" />



## RESULT:

The program successfully creates two threads, sets their names and priorities, and displays their details.
