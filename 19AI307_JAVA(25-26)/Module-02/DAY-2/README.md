# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.
When staticMethod() is called, it should print  "I am static".
When nonStaticMethod() is called, it should print  "I am non-static"

## AIM:
To write a Java program that demonstrates the use of one static method and one non-static method, and to call both from the main() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class containing one static method that prints "I am static".
4. Define one non-static (instance) method that prints "I am non-static".
5. In the main() method, directly call the static method using the class name or directly since it belongs to the same class.
6. Create an object of the class inside the main() method.
7. Using the object reference, call the non-static method and display the output.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
public class java{
    public static void main(String args[]){
        java obj=new java();
        method();
        obj.method1();
    }
    static void method(){
        System.out.print("I am static\n");
    }
    void method1(){
        System.out.print("I am non-static");
    }
}
```



## OUTPUT:

<img width="432" height="160" alt="image" src="https://github.com/user-attachments/assets/038e5e0f-96d6-4608-92ad-ae56f203aad0" />


## RESULT:
Thus, the program successfully demonstrated calling both a static method and a non-static method from the main() method, printing the respective messages.
