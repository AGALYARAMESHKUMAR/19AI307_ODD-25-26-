# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
To write a Java program using the Abstract Factory Design Pattern that creates animal families (Herbivore and Carnivore) from two regions — Africa and Asia, and prints their interaction where the carnivore eats the herbivore.

## ALGORITHM :
```
1. Start the program.
2. Import the necessary package 'java.util'
3. Define abstract interfaces:
    (a) Herbivore
  	 (b) Carnivore
    (c) AnimalFactory (returns herbivore & carnivore)
4. Implement African animals.
5. Implement Asian animals.
6. Create two concrete factories.
7. In the main class.
8. End program.
```





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}

class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Goat implements Herbivore {}

class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface ContinentFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements ContinentFactory {
    public Herbivore createHerbivore() {
        return new Wildebeest();
    }
    public Carnivore createCarnivore() {
        return new Lion();
    }
}

class AsiaFactory implements ContinentFactory {
    public Herbivore createHerbivore() {
        return new Goat();
    }
    public Carnivore createCarnivore() {
        return new Tiger();
    }
}


public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().trim().toLowerCase();

        ContinentFactory factory = null;

        if (region.equals("africa")) {
            factory = new AfricaFactory();
        } else if (region.equals("asia")) {
            factory = new AsiaFactory();
        } else {
            System.out.println("Invalid region");
            return;
        }

        Herbivore herb = factory.createHerbivore();
        Carnivore carn = factory.createCarnivore();

        carn.eat(herb);
    }
}
```






## OUTPUT:

<img width="1328" height="391" alt="image" src="https://github.com/user-attachments/assets/8eb39fd9-23c4-495a-bb11-1797c0ca6ae0" />


## RESULT:
The program successfully demonstrates the Abstract Factory Pattern by creating families of animals from multiple regions (Africa and Asia) and printing the interaction between carnivores and herbivores.

