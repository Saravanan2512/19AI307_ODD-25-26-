# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Define class Game with: Static variable maxScore = 500 Print max score via 3 different object references. Change via one object into 800, and print the output of previous maxScore and changed maxScore. 

## AIM:
To write a Java program that demonstrates the use of a static variable in a class by accessing it through multiple objects and modifying it using one object.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class game with a static variable maxscore initialized to 500.
4. Create multiple objects of the class and print the static variable through each object.
5. Create another object with a parameterized constructor that changes the static variable to 800.
6. Print the updated value using the modifying object.
7. Create more objects and print the static variable to show that the updated static value is shared across all objects.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
class game{
static int maxscore=500;

game(){
    // maxscore=0;
}
game(int m){
maxscore=m;
}
}
public class main{
public static void main(String args[]){
game ob=new game();
System.out.println(ob.maxscore);
game ob1=new game();
System.out.println(ob1.maxscore);
game ob2=new game();
System.out.println(ob2.maxscore);
game ob3=new game(800);
System.out.println(ob3.maxscore);
game ob4=new game(800);
System.out.println(ob4.maxscore);
game ob5=new game(800);
System.out.println(ob5.maxscore);
}
}
```


## OUTPUT:
<img width="266" height="269" alt="image" src="https://github.com/user-attachments/assets/63a5691d-ff3b-433a-bf70-0f184a934870" />



## RESULT:
Thus, the program successfully demonstrated that a static variable is shared by all objects of a class. Changing the static value using one object updated the value for all other objects as well.
