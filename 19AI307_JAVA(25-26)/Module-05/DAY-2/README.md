# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

## AIM:
To write a UTF-encoded string to a file using DataOutputStream and read it back using DataInputStream.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Accept a string input from the user.
4. Create a DataOutputStream and write the string using writeUTF().
5. Close the output stream to save data safely.
6. Create a DataInputStream and read the UTF string using readUTF().
7. Display the string read back from the file.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: SARAVANAN G
RegisterNumber: 212223230194
*/
import java.io.*;
import java.util.Scanner;

public class DataInputStreamUTFExample {
    public static void main(String[] args) {
        String fileName = "utfdata.dat";
        Scanner scanner = new Scanner(System.in);

        try {
            // Read input from user
            String input = scanner.nextLine();

            // --- Write UTF string to file ---
            DataOutputStream dos = new DataOutputStream(new FileOutputStream(fileName));
            dos.writeUTF(input);
            dos.close();

            // --- Read UTF string from file ---
            DataInputStream dis = new DataInputStream(new FileInputStream(fileName));
            String output = dis.readUTF();
            dis.close();

            System.out.println("String read from file: " + output);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }

        scanner.close();
    }
}
```


## OUTPUT:

<img width="746" height="252" alt="image" src="https://github.com/user-attachments/assets/53c38103-6cf7-4132-a1c4-54275962ffaa" />



## RESULT:
The program successfully writes a UTF string to a file (utfdata.dat) and reads it back using DataInputStream, displaying:

