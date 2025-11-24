# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.


## AIM:
To design a Java program using the Mediator Design Pattern where multiple airplane objects request landing permission through a central Air Traffic Controller. The mediator manages landing order and avoids collision.

## ALGORITHM :
```
1. Start the program.
2. Import the necessary package 'java.util'
3. Create a Mediator interface (ATCMediator) with methods to request and grant landing.
4. Implement it using a Concrete Mediator (ATCController) that manages a queue of landing requests.
5. Create an Airplane class having a name and a reference to the mediator.
6. Each airplane calls the mediator to submit a landing request.
7. The mediator grants landing permission one by one from the queue.
8. Display which airplane is landing using messages.
```




## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Agalya R
RegisterNumber: 212222040003
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
<img width="1267" height="662" alt="image" src="https://github.com/user-attachments/assets/3c4baed6-4e68-461c-a774-1561206e2301" />



## RESULT:

The program successfully implements the Mediator Design Pattern. All airplane landing requests are processed through a single Air Traffic Controller, which manages landing order and ensures controlled and safe landing.

