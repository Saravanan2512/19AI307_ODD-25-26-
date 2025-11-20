# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 

## AIM:
To read user input from the keyboard using InputStreamReader and BufferedReader in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an InputStreamReader object to read bytes from the keyboard.
4. Wrap it in a BufferedReader to read text efficiently.
5. Use readLine() to read a full line of user input as a string.
6. Store the input in a variable and process/display it.
7. Handle possible input exceptions using a try–catch block.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.io.*;

public class Main {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);

            String name = br.readLine();   // Read user input
            System.out.println("Hello, " + name + "!");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```


## OUTPUT:

<img width="473" height="198" alt="image" src="https://github.com/user-attachments/assets/14868966-43d2-40d9-a96b-07089d75353c" />



## RESULT:
The program successfully reads a user-entered string using InputStreamReader and prints a greeting message.
