# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
```
Write a Java program to reverse a number using a while loop. For example, if the input is 1234, the output should be 4321
```

## AIM:
To write a Java program to reverse a given number using a while loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Initialize a variable to store the reversed number (e.g., c = 0).
4. Use a while loop that runs until the number becomes zero.
5. Extract the last digit using modulus, append it to the reversed number, and reduce the original number by dividing by 10.
6. After the loop ends, print the reversed number.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by:  SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.*;
public class java{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int a= sc.nextInt();
        int c=0;
        while(a!=0){
            int b=a%10;
            c=c*10+b;
            a=a/10;
        }
        System.out.println("Reversed number: "+c);
    }
}
```


## OUTPUT:
<img width="584" height="233" alt="image" src="https://github.com/user-attachments/assets/d039d5e3-1561-49ee-bc52-4f21343c19df" />



## RESULT:
Thus, the program successfully reverses the given number using a while loop and displays the reversed output.
