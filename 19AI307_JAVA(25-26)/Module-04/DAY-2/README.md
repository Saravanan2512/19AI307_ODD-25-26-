# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

## AIM:
To implement a Singleton Design Pattern in Java by creating a single shared Print Spooler Manager that handles all print job submissions from multiple departments.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a PrintSpooler class with a private static instance to ensure only one object is created.
4. Make the constructor private to prevent creating additional objects externally.
5. Provide a public static method getInstance() to return the single spooler instance.
6. Maintain a shared jobCount variable that increments whenever any department submits a job.
7. In main(), read the number of departments and process each print job by calling submitJob() through the singleton instance.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.*;

// Singleton class
class PrintSpooler {
    private static PrintSpooler instance;  // single instance
    private int jobCount = 0;              // shared state across departments

    // private constructor prevents multiple instances
    private PrintSpooler() {}

    // global access point to get the single instance
    public static PrintSpooler getInstance() {
        if (instance == null) {
            instance = new PrintSpooler();
        }
        return instance;
    }

    // method to submit a print job
    public void submitJob(String department) {
        jobCount++;
        System.out.println(department + " submitted a print job. Total Jobs in Queue: " + jobCount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            String department = sc.nextLine();

            // every department accesses the same shared instance
            PrintSpooler spooler = PrintSpooler.getInstance();
            spooler.submitJob(department);
        }

        sc.close();
    }
}
```


## OUTPUT:

![Uploading image.png…]()


## RESULT:
The program successfully demonstrates the Singleton pattern by using one shared PrintSpooler instance to manage all print jobs globally.
