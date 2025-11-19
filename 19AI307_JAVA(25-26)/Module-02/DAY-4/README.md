# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Create a Java class Book with instance variables title and author.

## AIM:
To create a Java class Book (here implemented as java) with instance variables for title and author, and to display the book details using a method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Begin by creating a class with two instance variables to store the book title and author name.
4. Define a parameterized constructor to initialize these instance variables with user-entered values.
5. Create a method to print the title and author in a formatted manner.
6. In the main() method, read the book title and author name from the user.
7. Create an object of the class, pass the values to the constructor, and call the method to display the book details.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: SARAVANAN g
RegisterNumber:  212223230194
*/
import java.util.*;
public class main{
public static void main(String args[]){
 Scanner sc=new Scanner(System.in);
String s1=sc.nextLine();
// sc.nextLine();
String s2=sc.nextLine();
// String s1="C programming";
// String s2="Dennis Ritche";

java ob=new java(s1,s2);
ob.printstring();
}
}
class java{
String s3,s4;
java(String s1, String s2){
s3=s1;
s4=s2;
}
void printstring(){
System.out.println("Book Title: "+s3);
System.out.println("Author: "+s4);
}
}

```

## OUTPUT:
<img width="820" height="305" alt="image" src="https://github.com/user-attachments/assets/a586f998-ad87-4efb-91c0-54caf2ec2dc8" />



## RESULT:
Thus, the program successfully created a class with instance variables for a book’s title and author, accepted input from the user, and displayed the book details correctly.

