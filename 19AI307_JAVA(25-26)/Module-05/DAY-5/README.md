# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use ScheduledExecutorService to delay execution of tasks and print their message.

## AIM:
To schedule multiple tasks with different delays using ScheduledExecutorService.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of tasks from the user.
4.	Create a ScheduledExecutorService with a thread pool of size n.
5.	For each task, read a message and a delay value.
6.	Schedule each message to be printed after the specified delay using scheduler.schedule().
7.	Shut down the scheduler after scheduling all tasks.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt(); // number of tasks
        ScheduledExecutorService scheduler = Executors.newScheduledThreadPool(n);

        for (int i = 0; i < n; i++) {
            String message = sc.next();
            int delay = sc.nextInt();

            scheduler.schedule(() -> {
                System.out.println(message);
            }, delay, TimeUnit.SECONDS);
        }

        scheduler.shutdown();
        sc.close();
    }
}

```






## OUTPUT:

<img width="421" height="578" alt="image" src="https://github.com/user-attachments/assets/43773724-6856-4658-bde3-66094ce86a95" />


## RESULT:

The program successfully schedules and prints messages after their respective delays using ScheduledExecutorService.
