# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## AIM:
To Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read inputs: number of airplanes and runway status (free or busy).
4.	Create one AirTrafficControl object and read all airplane names into a list.
5.	If the runway is free, allow all airplanes to land by calling requestGrant().
6.	If the runway is busy, allow only the first airplane to land and deny landing for all others.
7.	Print landing or denial messages for each airplane accordingly.
8.	End
   
## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044

*/
```

## SOURCE CODE:
```
import java.util.*;

class AirTrafficControl {
    public void grantLanding(Airplane plane) {
        System.out.println(plane.getName() + " granted landing.");
        System.out.println(plane.getName() + " landed successfully.");
    }

    public void denyLanding(Airplane plane) {
        System.out.println(plane.getName() + " denied landing. Runway busy.");
    }
}

class Airplane {
    private String name;
    private AirTrafficControl atc;

    public Airplane(String name, AirTrafficControl atc) {
        this.name = name;
        this.atc = atc;
    }

    public String getName() {
        return name;
    }

    public void requestGrant() {
        atc.grantLanding(this);
    }

    public void requestDeny() {
        atc.denyLanding(this);
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextInt()) {
            int n = sc.nextInt();
            if (!sc.hasNext()) break;
            boolean runwayFree = sc.nextBoolean();
            sc.nextLine(); 

            AirTrafficControl atc = new AirTrafficControl();
            List<Airplane> planes = new ArrayList<>();

            for (int i = 0; i < n; i++) {
                if (!sc.hasNextLine()) break;
                String name = sc.nextLine().trim();
                planes.add(new Airplane(name, atc));
            }

            if (runwayFree) {
                for (Airplane p : planes) {
                    p.requestGrant();
                }
            } else {
                for (int i = 0; i < planes.size(); i++) {
                    Airplane p = planes.get(i);
                    if (i == 0) {
                        p.requestGrant();
                    } else {
                        p.requestDeny();
                    }
                }
            }
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1239" height="676" alt="image" src="https://github.com/user-attachments/assets/a9c20b8d-c606-4331-8dec-b2a14ddf6273" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


