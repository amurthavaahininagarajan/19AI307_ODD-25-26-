# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()


## AIM:
To set and display an employee’s name using method returning and method chaining.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Employee class with a name variable.
4.Define setName() to assign the employee name.
5.Define display() to return the current object using this.
6.Define printName() to print the employee name.
7.In main, read the employee name, set it using setName(), and print it using method chaining.
```




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Employee {
    String name;
    void setName(String name) {
        this.name = name; 
    }
    Employee display() {
        return this; 
    }
    void printName() {
        System.out.println("Employee Name: " + name);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();

        Employee emp = new Employee();
        emp.setName(name);
        emp.display().printName(); 
    }
}
```






## OUTPUT:

<img width="664" height="335" alt="image" src="https://github.com/user-attachments/assets/f6bedd28-984a-46e7-aeec-5fe424dc4af3" />


## RESULT:
The program successfully reads, stores, and displays the employee’s name using method chaining.

