# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to calculate an employee's salary using method overloading.

## AIM:
To write a Java program that calculates an employee's salary using method overloading, with one method applying a 20% allowance and another applying a user-provided bonus.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Salary containing two calculate() methods with different parameter lists to demonstrate method overloading.
4. In the first calculate(double baseSalary) method, compute the net salary by adding a 20% allowance to the base salary.
5. In the second overloaded calculate(double baseSalary, double bonus) method, compute the net salary by adding the bonus to the base salary.
6. In the main() method, read the base salary and ask the user whether a bonus should be added.
7. Based on the user’s choice, call the appropriate overloaded method and display the calculated net salary.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

public class Salary {

    // Method to calculate salary without bonus (20% allowance)
    public void calculate(double baseSalary) {
        double netSalary = baseSalary + (0.20 * baseSalary);
        System.out.println("Net Salary (20% allowance): ₹" + netSalary);
    }

    // Overloaded method to calculate salary with bonus
    public void calculate(double baseSalary, double bonus) {
        double netSalary = baseSalary + bonus;
        System.out.println("Net Salary with bonus: ₹" + netSalary);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Salary s = new Salary();

        double base = sc.nextDouble();

        sc.nextLine(); // consume leftover newline
        
        String choice = sc.nextLine();

        if (choice.trim().equalsIgnoreCase("yes")) {
            
            double bonus = sc.nextDouble();
            s.calculate(base, bonus); // call overloaded method with bonus
        } else {
            s.calculate(base); // call method without bonus
        }

        sc.close();
    }
}

```


## OUTPUT:
<img width="857" height="352" alt="image" src="https://github.com/user-attachments/assets/e858af73-7121-4bd5-a7a0-12da5c53e2f7" />



## RESULT:
Thus, the program successfully demonstrated method overloading by computing the employee’s salary either with a 20% allowance or with an additional bonus based on user input.
