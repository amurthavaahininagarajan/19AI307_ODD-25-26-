# Ex.No:3(D)    INTERFACE 

## QUESTION:
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.


AggressiveController: Allows only if "GREEN".

DefensiveController: Allows for "GREEN" or "YELLOW".
## AIM:

To decide traffic movement based on signal color using interfaces and different controller implementations.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a TrafficController interface with the decide() method.
4.	Implement AggressiveController to allow movement only on GREEN.
5.	Implement DefensiveController to allow movement on GREEN or YELLOW.
6.	Implement DefensiveController to allow movement on GREEN or YELLOW.
7.	Create the appropriate controller object and display the decision returned by decide()




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface TrafficController {
    String decide(String signalColor);
}
class AggressiveController implements TrafficController {
    public String decide(String signalColor) {
        if (signalColor.equalsIgnoreCase("GREEN"))
            return "GO";
        else
            return "STOP";
    }
}
class DefensiveController implements TrafficController {
    public String decide(String signalColor) {
        if (signalColor.equalsIgnoreCase("GREEN") || signalColor.equalsIgnoreCase("YELLOW"))
            return "GO";
        else
            return "STOP";
    }
}
public class TrafficControllerSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String signalColor = sc.next().trim().toUpperCase();
        int controllerType = sc.nextInt();

        TrafficController controller;

        if (controllerType == 1) {
            controller = new AggressiveController();
        } else if (controllerType == 2) {
            controller = new DefensiveController();
        } else {
            System.out.println("Invalid controller type.");
            sc.close();
            return;
        }
        System.out.println(controller.decide(signalColor));
        sc.close();
    }
}
```






## OUTPUT:

<img width="505" height="331" alt="image" src="https://github.com/user-attachments/assets/c194ac3a-4f6e-4941-8664-85bc1c59912d" />


## RESULT:
The program successfully determines whether to GO or STOP based on the signal color and controller type using interface implementation.
