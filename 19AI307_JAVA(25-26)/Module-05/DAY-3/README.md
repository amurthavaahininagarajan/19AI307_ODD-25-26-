# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Write a program to count the number of words in a file.
## AIM:
To count the number of words in the given input text.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a line of text from the user.
4.	Trim the text to remove leading and trailing spaces.
5.	Split the text into words using whitespace as the delimiter.
6.	Count the number of words obtained from the split operation.
7.	Display the total word count.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class WordCount {
    public static void main(String[] args) throws IOException {
        Scanner sc = new Scanner(System.in);
        String content = sc.nextLine();
        String[] words = content.trim().split("\\s+");
        System.out.println("Number of words in the file: " + words.length);
    }
}
```






## OUTPUT:

<img width="1175" height="334" alt="image" src="https://github.com/user-attachments/assets/e342bc5a-ddd8-4596-b38e-72e491c70b53" />


## RESULT:

The program successfully counts and displays the number of words in the given text.
