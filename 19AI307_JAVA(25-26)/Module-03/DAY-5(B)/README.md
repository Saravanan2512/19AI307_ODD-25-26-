# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 

## AIM:
To write a Java program that checks whether a given number is prime or not using the Integer wrapper class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer using the Integer wrapper class.
4. Initialize a boolean variable to track if the number is prime.
5. Use a loop to check divisibility from 2 to √n.
6. Display whether the number is prime or not based on the check.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer num = sc.nextInt(); // using wrapper class Integer

        boolean isPrime = true;

        if (num <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime)
            System.out.println(num + " is a prime number.");
        else
            System.out.println(num + " is not a prime number.");
    }
}
```



## OUTPUT:
<img width="710" height="241" alt="image" src="https://github.com/user-attachments/assets/e186c392-d05f-4106-b4cd-8d56ed0c2e78" />



## RESULT:

The program successfully determines whether the given number is a prime number using the Integer wrapper class, and displays the correct output.
