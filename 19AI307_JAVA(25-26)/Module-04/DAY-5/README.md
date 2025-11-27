# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento design pattern to store multiple versions of an article and restore a selected version.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Memento class to store a snapshot of article content.
4.	Create an Article class that maintains a history list of Memento objects.
5.	On each new content input, store it as a new Memento in the history.
6.	Read the version number to restore.
7.	If version is 0, print the first saved content; if version exceeds history size, print “Invalid version”; otherwise print the latest content.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.*;

class Memento {
    private String content;
    public Memento(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }
}

class Article {
    private List<Memento> history = new ArrayList<>();

    public void setContent(String content) {
        history.add(new Memento(content));
    }

    public void restore(int version) {
        if (version == 0) {
            System.out.println(history.get(0).getContent());
        } else if (version > history.size()) {
            System.out.println("Invalid version");
        } else {
            System.out.println(history.get(history.size() - 1).getContent());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        Article article = new Article();
        for (int i = 0; i < n; i++) {
            article.setContent(sc.nextLine());
        }

        int versionToRestore = sc.nextInt();
        article.restore(versionToRestore);
    }
}
```






## OUTPUT:

<img width="813" height="534" alt="image" src="https://github.com/user-attachments/assets/89362650-6ec1-4859-af08-348471154aee" />


## RESULT:

The program successfully saves multiple versions of an article and restores the appropriate version using the Memento design pattern.
