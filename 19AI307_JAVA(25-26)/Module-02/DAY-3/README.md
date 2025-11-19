# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

## AIM:
To create a Java class Rectangle (here implemented as Person) with private instance variables length and width, and to access/modify them using public getter and setter methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class with two private variables: length and width.
4. Create public getter methods to return the values of length and width.
5. Create public setter methods to assign values to these private variables.
6. In the main() method, create an object of the class.
7. Use setter methods to store user-entered values and getter methods to display the values.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;
class Person{
        private double length;
        private double width;
        
        public double getLength(){
            return length;
        }
        public void setLength(double length){
            this.length=length;
        }
        public double getWidth(){
            return width;
        }
        public void setWidth(double width){
            this.width=width;
        }
}
public class Main
{
 public static void main(String arg[]){   
            Scanner sc=new Scanner(System.in);
            Person ob=new Person();
            ob.setLength(sc.nextDouble());
            ob.setWidth(sc.nextDouble());
            double a=ob.getLength();
            double b=ob.getWidth();
            System.out.println("Length: "+a);
            System.out.println("Width: "+b);
        
        
    }
}

```

## OUTPUT:

<img width="608" height="370" alt="image" src="https://github.com/user-attachments/assets/2a2c0813-31c4-416f-b514-daf330f4ffc4" />


## RESULT:
Thus, the program successfully demonstrated encapsulation by using private variables along with public getter and setter methods to read and display the length and width values.
