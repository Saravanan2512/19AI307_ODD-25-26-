# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2
## AIM:
To write a Java program that sets and displays the name and priority of the current threads. The program should accept two thread names from the user and assign different priorities to each thread.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create two thread objects with these names.
4. Set priorities for threads (t1=4, t2=2).
5. Print each thread’s name and priority.
6. Close the scanner.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

class MyThread extends Thread {
    public MyThread(String name) {
        super(name);
    }

    @Override
    public void run() {
        // No task needed, we just need thread info
    }
}

public class ThreadPriorityExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Read thread names
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        // Create threads with user-given names
        MyThread t1 = new MyThread(name1);
        MyThread t2 = new MyThread(name2);

        // Set priorities
        t1.setPriority(4);
        t2.setPriority(2);

        // Print thread info
        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```


## OUTPUT:


<img width="773" height="238" alt="image" src="https://github.com/user-attachments/assets/96b97644-4cb7-4d7a-b6b4-ace9798556de" />


## RESULT:
Thread information with assigned name and priority is displayed on the screen
