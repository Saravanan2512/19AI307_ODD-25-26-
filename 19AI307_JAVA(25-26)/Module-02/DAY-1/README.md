# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To create a class Vehicle with attributes number, type, and owner, and to read and display the details of two vehicle objects using user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to take user input.
4. Create two objects of the Vehicle class (v1 and v2).
5.For each object, read the values of number, type, and owner from the user.
6.Display the details of both vehicles in a formatted manner.
7.Close the Scanner object.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

public class Vehicle {
    String  number="";
    String type="";
    String owner="";
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}

```


## OUTPUT:
<img width="804" height="227" alt="image" src="https://github.com/user-attachments/assets/0b0460fe-0708-4f46-9824-ca1ecbeaffbe" />



## RESULT:
Thus, the program successfully created a Vehicle class, accepted details for two vehicles from the user, and displayed their information in the required format.
