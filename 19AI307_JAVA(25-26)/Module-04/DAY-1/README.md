# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write a Java program that checks whether a string is null before converting it to uppercase, in order to avoid a NullPointerException.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string from the user.
4. Check if the string is null or equal to the text "null".
5. If it is null, display "Null element".
6. Otherwise, convert the string to uppercase using .toUpperCase() and print it.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine(); 
        if (input == null || input.equalsIgnoreCase("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(input.toUpperCase());
        }

        sc.close();
    }
}

```


## OUTPUT:
<img width="504" height="240" alt="image" src="https://github.com/user-attachments/assets/810abdbc-ef28-4d53-9c56-29aabe3cb43c" />



## RESULT:
The program successfully identifies null inputs and prevents a NullPointerException by checking the string before calling .toUpperCase().
Valid strings are converted to uppercase and displayed correctly.
