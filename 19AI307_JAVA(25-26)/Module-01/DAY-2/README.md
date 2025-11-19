# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
```
Given a month number (1 to 12), print which quarter of the year it belongs to:
Months 1,2,3 → "First Quarter"
Months 4,5,6 → "Second Quarter"
Months 7,8,9 → "Third Quarter"
Months 10,11,12 → "Fourth Quarter"
If the number is not in 1-12, print "Invalid Month".
Write a java program to get the month from user and and display appropriate output for the given input.


```

## AIM:
To write a Java program that accepts a month number from the user and displays the corresponding quarter of the year.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Accept an integer input representing the month (1–12).
4. Check whether the month falls in the ranges 1–3, 4–6, 7–9, or 10–12.
5. Display the appropriate quarter based on the month range.
6. If the entered number is outside 1–12, display “Invalid Month”.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by:  SARAVANAN G
RegisterNumber:  212223230194
*/

import java.util.Scanner;

public class MonthQuarter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int month = sc.nextInt();
        sc.close();

        if (month >= 1 && month <= 3) {
            System.out.println("First Quarter");
        } else if (month >= 4 && month <= 6) {
            System.out.println("Second Quarter");
        } else if (month >= 7 && month <= 9) {
            System.out.println("Third Quarter");
        } else if (month >= 10 && month <= 12) {
            System.out.println("Fourth Quarter");
        } else {
            System.out.println("Invalid Month");
        }
    }
}
```

## OUTPUT:
<img width="473" height="152" alt="image" src="https://github.com/user-attachments/assets/a465cbaa-63cc-4789-b1b1-17e68a32f277" />



## RESULT:
Thus, the program successfully reads a month number from the user and displays its corresponding quarter or shows an invalid message for out-of-range values.
