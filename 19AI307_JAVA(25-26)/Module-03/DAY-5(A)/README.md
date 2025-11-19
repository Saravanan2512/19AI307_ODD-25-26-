# Ex.No:3(E) INNER CLASS

## QUESTION:
Write an enum VehicleType (CAR, BIKE, BUS) with a constructor that takes number of wheels. Print wheel count for each.

## AIM:
To create a Java program that uses an enum to display the number of wheels for a selected vehicle type.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the vehicle type input from the user.
4. Convert the input to uppercase to match enum constants.
5. Use valueOf() to get the corresponding enum value.
6. Access the wheel count using the getWheels() method.
7. Display the vehicle name and number of wheels, or show an error for invalid input.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: SARAVANAN G
RegisterNumber: 212223230194 
*/
import java.util.Scanner;

enum VehicleType {
    CAR(4),
    BIKE(2),
    BUS(6);

    private int wheels;

    VehicleType(int wheels) {
        this.wheels = wheels;
    }

    public int getWheels() {
        return wheels;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.next().toUpperCase(); // read user input (e.g., "car")
        
        try {
            VehicleType v = VehicleType.valueOf(input);
            System.out.println(v + " has " + v.getWheels() + " wheels.");
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid vehicle type entered.");
        }
    }
}
```

## OUTPUT:
<img width="740" height="232" alt="image" src="https://github.com/user-attachments/assets/88596ee2-eb40-4d46-89c2-a9e28c14c835" />



## RESULT:
The program successfully retrieves the correct enum value, displays the wheel count for CAR, BIKE, or BUS, and handles invalid inputs gracefully.
