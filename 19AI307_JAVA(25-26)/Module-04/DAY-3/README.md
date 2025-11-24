# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A Department contains Professor objects, but professors can exist independently.
If no inputs gets passed, print "No professors assigned."

## AIM:
To write a Java program where a Department contains Professor objects, but Professor objects can exist independently. If no professors are assigned to a department, the message "No professors assigned." must be printed.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a Professor class containing professor details (like name).
4.Create a Department class containing:
   (a) department name
   (b) a list/array of professors
5.If no professors are passed to the department, display "No professors assigned."
6.If professors are passed, display the department name and professor names.
7.Demonstrate both cases in the main() method.
```





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:

```
import java.util.*;

class Professor {
    private String name;

    public Professor(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

class Department {
    private String deptName;
    private List<Professor> professors; // Aggregation

    public Department(String deptName) {
        this.deptName = deptName;
        this.professors = new ArrayList<>();
    }

    public void addProfessor(Professor p) {
        professors.add(p);
    }

    public void displayProfessors() {
        System.out.println("Department: " + deptName);

        if (professors.isEmpty()) {
            System.out.println("No professors assigned.");
            return;
        }

        for (Professor p : professors) {
            System.out.println("- " + p.getName());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int count = Integer.parseInt(sc.nextLine());
        List<Professor> profList = new ArrayList<>();

        for (int i = 0; i < count; i++) {
            String name = sc.nextLine();
            profList.add(new Professor(name));
        }

        Department dept = new Department("Computer Science");

        for (Professor p : profList) {
            dept.addProfessor(p);
        }

        dept.displayProfessors();
    }
}
```





## OUTPUT:

<img width="1115" height="296" alt="image" src="https://github.com/user-attachments/assets/3de6a7b2-73a2-4337-8823-68e4e9ca8b73" />



## RESULT:
The program demonstrates that a Department contains Professor objects (Aggregation) and that Professors can exist independently. When a department has no assigned professors, the message "No professors assigned." is printed successfully.

