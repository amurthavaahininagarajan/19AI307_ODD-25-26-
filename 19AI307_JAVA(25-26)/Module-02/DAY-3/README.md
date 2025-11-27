# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

## AIM:
To read and display the length and width of a rectangle using getter and setter methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with private variables length and width.
4.Define setter methods to assign values to length and width.
5.Define getter methods to retrieve length and width.
5.In main, read length and width from the user and set them using setter methods.
6.Print the values using getter methods.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class prog {
    private double length;
    private double width;
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        prog rect = new prog();
        rect.setLength(sc.nextDouble());
        rect.setWidth(sc.nextDouble());
        System.out.println("Length: " + rect.getLength());
        System.out.println("Width: " + rect.getWidth());
    }
}
```




## OUTPUT:

<img width="553" height="393" alt="image" src="https://github.com/user-attachments/assets/b8696bbd-8800-4f9e-a36e-098e25c60c1a" />


## RESULT:
The program successfully reads the rectangle dimensions and displays them using getter and setter methods.
