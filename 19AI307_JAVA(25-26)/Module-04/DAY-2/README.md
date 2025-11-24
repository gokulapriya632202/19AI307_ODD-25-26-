# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.
To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.
Your task is to simulate this system using the Singleton pattern.

## AIM:
To ensure all flights use one shared Radar Control Tower by implementing the Singleton pattern, and to record each flight’s registration in the order they contact the tower.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input from user.
4.	Get the same RadarControlTower instance using getInstance().
5.	Register the flight by increasing the flight count.
6.	Print the flight name and the updated total number of registered flights.
7.	End

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: GOKULA PRIYA P
RegisterNumber: 212222040044 
*/
```

## SOURCE CODE:
```
import java.util.*;
class RadarControlTower {
    private static RadarControlTower instance; 
    private int flightCount; 
    private RadarControlTower() {
        flightCount = 0;
    }
    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }
    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine(); 
        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance(); 
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```

## OUTPUT:
<img width="1255" height="332" alt="image" src="https://github.com/user-attachments/assets/1285f92f-6829-4af6-aaa7-64d0b01c607d" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


