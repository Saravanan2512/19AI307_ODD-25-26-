# Ex.No:1(D) ARRAYS

## QUESTION:
```
Write a Java program to print all elements in an array that are greater than a given value
```


## AIM:


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Input all the array elements from the user and store them in an integer array.
4. Read the comparison value from the user.
5. Traverse the array and print all elements that are greater than the given value.
6. If no such element is found, display a message saying “No elements greater than <value>”.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by:  SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);

        int n = scan.nextInt();   
        int arr[] = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = scan.nextInt();
        }

        int value = scan.nextInt();   

        boolean found = false;
        for (int i = 0; i < n; i++) {
            if (arr[i] > value) {
                System.out.println(arr[i]);
                found = true;
            }
        }

        if (!found) {
            System.out.println("No elements greater than " + value);
        }
    }
}
```


## OUTPUT:
<img width="674" height="222" alt="image" src="https://github.com/user-attachments/assets/5fad51d1-f137-4e9a-9a72-e2d9f3389edf" />



## RESULT:
Thus, the Java program successfully reads an array and a comparison value, and it correctly displays all elements greater than the given value or shows an appropriate message when no such elements are f

