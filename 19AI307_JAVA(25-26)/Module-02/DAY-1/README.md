# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To create a Vehicle class and read the details of two vehicles and display them.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a Vehicle class with number, type, and owner as data members.
4.Create two Vehicle objects.
5.Read number, type, and owner for the first vehicle.
6.Read number, type, and owner for the second vehicle.
7.Print the details of both vehicles in the given format.
RESULT: The program successfully reads and displays the details of two vehicles.




## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Vehicle {
    String number;
    String type;
    String owner;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}
```




## OUTPUT:
<img width="875" height="325" alt="image" src="https://github.com/user-attachments/assets/1801837a-f170-46a9-9bf2-461d8af5dcfa" />



## RESULT:

The program successfully reads and displays the details of two vehicles.
