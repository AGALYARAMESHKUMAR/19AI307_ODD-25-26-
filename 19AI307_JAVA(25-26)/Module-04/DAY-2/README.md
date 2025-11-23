# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.

The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.

Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

Hidden Clue:
Use Singleton to manage shared access.

Count and log each print job submission.

Validate that state is preserved across all accesses.

Input Format:
First line: Integer n – number of print jobs

Next n lines: Each line contains the department name submitting the print job.

Output Format:
For each job, print:


[Department] submitted a print job. Total Jobs in Queue: [count]

## AIM:
To write a Java program that simulates a centralized print spooler using the Singleton Design Pattern, ensuring that only one spooler manager instance exists and all departments submit print jobs to this single instance while maintaining a shared job count.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a Singleton class PrintSpooler with:
    ->A private static instance reference.
    ->A private constructor.
    ->A static method getInstance() to return the single instance.
    ->A variable count to store number of print jobs.
    ->A method submitJob() to increment count and print the message.
 4.Read n, the number of print jobs.
 5.For each job:
     ->Read department name.
     ->Get the spooler instance using getInstance().
     ->Call submitJob(departmentName).
6.Display the message after each submission.
7.End the program.
```




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Mythili D
RegisterNumber: 212222040104 
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance; 
    private int jobCount; 
    private PrintSpoolerManager() {
        jobCount = 0;
    }
    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }
    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {

            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance(); 
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```







## OUTPUT:
<img width="1219" height="484" alt="image" src="https://github.com/user-attachments/assets/3627e70c-3efe-4b70-b033-7fd3fcb4c5ba" />



## RESULT:
The program successfully implements a Singleton Print Spooler Manager where all departments share a single print job queue instance, proving that all job submissions update the same shared state.
