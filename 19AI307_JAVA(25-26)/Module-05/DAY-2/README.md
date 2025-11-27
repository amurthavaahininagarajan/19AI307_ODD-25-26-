# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.

## AIM:

To store user-entered UTF strings in memory using ByteArray streams and retrieve them back.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create ByteArrayOutputStream and DataOutputStream to store UTF strings in memory.
4.	Read the number of strings from the user.
5.	Read each string and write it into memory using writeUTF().
6.	Convert the stored data into a byte array and display its contents.
7.	Create ByteArrayInputStream and DataInputStream to read back the strings from memory.
8.	Read and display each UTF string using readUTF().





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class UTFStringsInMemoryUserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            // Create ByteArrayOutputStream to store data in memory
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            DataOutputStream dos = new DataOutputStream(baos);

            // Get number of strings from user
            int n = scanner.nextInt();
            scanner.nextLine(); // Consume newline

            // Read strings from user and write them in UTF format
            for (int i = 0; i < n; i++) {
                String str = scanner.nextLine();
                dos.writeUTF(str);
            }

            // Convert to byte array
            byte[] byteData = baos.toByteArray();

            // Display byte array contents
            System.out.println("Byte array contents:");
            for (byte b : byteData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + byteData.length);

            // Read strings back from memory
            ByteArrayInputStream bais = new ByteArrayInputStream(byteData);
            DataInputStream dis = new DataInputStream(bais);

            System.out.println("\nStrings read from memory:");
            for (int i = 0; i < n; i++) {
                System.out.println(dis.readUTF());
            }

            // Close streams
            dos.close();
            dis.close();

        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```






## OUTPUT:

<img width="1213" height="717" alt="image" src="https://github.com/user-attachments/assets/99d79d38-856c-43ef-b16a-b11b85d6160d" />


## RESULT:
The program successfully stores UTF strings in memory, displays the byte array, and retrieves the original strings using in-memory I/O streams.
