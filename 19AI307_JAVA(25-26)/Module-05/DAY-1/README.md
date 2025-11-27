# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write text into a file using FileOutputStream. 

## AIM:
To write a string into a file using FileOutputStream in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the file name and content from the user.
4.	Create a FileOutputStream object using the given file name.
5.	Convert the string content into bytes.
6.	Write the byte data into the file using FileOutputStream.
7.	Close the stream and display a success message.




## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.Scanner;

public class FileOutputStreamExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String fileName = scanner.nextLine();  
        String content = scanner.nextLine();   

        try {
            // Create FileOutputStream to write bytes to the file
            FileOutputStream fos = new FileOutputStream(fileName);

            // Convert string to bytes and write to file
            fos.write(content.getBytes());

            fos.close();
            System.out.println("File written successfully.");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```





## OUTPUT:

<img width="771" height="334" alt="image" src="https://github.com/user-attachments/assets/8b360c27-f64a-4896-b952-2783e25c6be9" />

## RESULT:

The program successfully writes the given text into the specified file using FileOutputStream.
