# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

## AIM:

To define a common interface for weather analysis bots that ensures consistent prediction behavior.
To implement multiple bot classes that analyze weather data and provide predictions using the interface.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create an interface WeatherBot with a method predict().
4.Implement the interface in two classes:
   1.SunBot
   ->If temperature > 30 → "HOT"
   ->Else → "MODERATE"
   2.RainBot
    ->If temperature < 20 → "COLD"
    ->Else → "WARM"
5.Read input:
    ->Temperature
    ->Bot type (1 for SunBot, 2 for RainBot)
6.If bot type is 1, create a SunBot object; else, create a RainBot object.
7.Call the predict() method and display the result.
8.End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.*;

interface WeatherBot {
    String predict(int temp);
}

class SunBot implements WeatherBot {
    public String predict(int temp) {
        return (temp > 30) ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temp) {
        return (temp < 20) ? "COLD" : "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temp = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1)
            bot = new SunBot();
        else if (botType == 2)
            bot = new RainBot();
        else {
            System.out.println("Invalid bot type!");
            return;
        }

        System.out.println(bot.predict(temp));
    }
}
```





## OUTPUT:
<img width="1190" height="305" alt="image" src="https://github.com/user-attachments/assets/a2a53943-7b1d-41ae-8edf-c17b68ce922f" />



## RESULT:
The program successfully uses an interface to generate weather predictions using SunBot and RainBot based on temperature.


