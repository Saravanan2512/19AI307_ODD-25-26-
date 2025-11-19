# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
```
Write a Java program to remove all vowels from a given string.
```

## AIM:
To write a Java program that removes all vowels from a given string and displays the modified string.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Initialize an empty string to store characters that are not vowels.
4. Traverse the input string character by character using a loop.
5. Check each character; if it is not a vowel (a, e, i, o, u in both cases), append it to the result string.
6. After processing all characters, display the final string without vowels.





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);
        String str = scan.nextLine();

        String result = "";
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            if ("AEIOUaeiou".indexOf(ch) == -1) {
                result += ch;
            }
        }

        System.out.println("String without vowels: " + result);
    }
}
```

## OUTPUT:

<img width="791" height="236" alt="image" src="https://github.com/user-attachments/assets/6b2ced82-9d5c-4ee9-9d43-2ebc40d19bde" />


## RESULT:
Thus, the program successfully removes all vowels from the given string and prints the resulting string without vowels.
