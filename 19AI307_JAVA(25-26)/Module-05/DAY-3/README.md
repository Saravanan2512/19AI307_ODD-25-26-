# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

## AIM:
To read lines from input and print only those that contain the word "Java".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BufferedReader to read text input line by line.
4. Continuously read lines until the user types "exit".
5. For each line, check if it contains the word "Java".
6. If it does, print that line.
7. Handle any input/output exceptions.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class FilterJavaLines {
    public static void main(String[] args) {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        System.out.println("Lines containing the word 'Java':");

        try {
            String line;
            while ((line = br.readLine()) != null) {
                if (line.equals("exit")) {
                    break;
                }
                if (line.contains("Java")) {
                    System.out.println(line);
                }
            }
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

## OUTPUT:


<img width="979" height="301" alt="image" src="https://github.com/user-attachments/assets/e5941655-d808-4770-b5e5-900fea9c524a" />


## RESULT:
The program successfully filters and displays only the lines that contain the word "Java" from the user’s input.
