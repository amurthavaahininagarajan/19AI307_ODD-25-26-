# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.

Each user has their own preference:

Some are looking for "Gamers"

Some prefer "Pet Lovers"

Others vibe with "Bookworms"

Or maybe they're into "Gym Freaks", etc.

When a new user signs up, the app should only notify users whose preferences match that new person’s type.

Users subscribe to MatchIt’s notification service based on their “match interest”. The system notifies them only when someone with their preferred type signs up.

What Students Must Do:
Implement the Observer Pattern

MatchItServer = Subject

User = Observer

When a new person joins, notify only users who match the preference

Each user prints a custom message when their preferred type joins.

## AIM:
To implement the Observer design pattern where users receive notifications about new sign-ups matching their preferences.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Observer interface with update() and getPreference() methods.
4.	Create a User class implementing Observer that stores name and preference.
5.	Create a Subject interface with methods to register users and notify them.
6.	Implement MatchItServer as the subject that stores users and sends notifications only to preferred users.
7.	In main, read existing users and their preferences, register them, read new sign-ups, and notify matching users.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
import java.util.*;

// Observer Interface
interface Observer {
    void update(String newUserName, String type);
    String getPreference();
}

// Concrete Observer
class User implements Observer {
    private String name;
    private String preference;

    public User(String name, String preference) {
        this.name = name;
        this.preference = preference;
    }

    @Override
    public void update(String newUserName, String type) {
        System.out.println(name + ": Omg! A new " + type + "? MatchIt, you know me too well! (It’s " + newUserName + "!)");
    }

    @Override
    public String getPreference() {
        return preference;
    }
}

// Subject Interface
interface Subject {
    void registerUser(User user);
    void notifyUsers(String newUserName, String type);
}

// Concrete Subject
class MatchItServer implements Subject {
    private List<User> users = new ArrayList<>();

    @Override
    public void registerUser(User user) {
        users.add(user);
    }

    @Override
    public void notifyUsers(String newUserName, String type) {
        System.out.println("New User Joined: " + newUserName + " - Type: " + type);
        for (User user : users) {
            if (user.getPreference().equalsIgnoreCase(type)) {
                user.update(newUserName, type);
            }
        }
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String userName = input[0];
            String preference = input[1];
            server.registerUser(new User(userName, preference));
        }

        int m = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < m; i++) {
            String[] signup = sc.nextLine().split(" ");
            String newUserName = signup[0];
            String type = signup[1];
            server.notifyUsers(newUserName, type);
        }

        sc.close();
    }
}
```





## OUTPUT:

<img width="1331" height="469" alt="image" src="https://github.com/user-attachments/assets/b853f96d-13e9-4bf8-b06b-9ff338189ad4" />


## RESULT:
The program successfully demonstrates the Observer pattern by notifying only those users whose preferences match the newly joined user’s type.

