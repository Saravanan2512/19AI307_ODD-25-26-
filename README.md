# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
```
Lovely wants to enter a secure tech conference. The security system checks certain conditions to grant access. These conditions are:
She must be registered (true/false).
She must have a valid ID (true/false.
She must NOT be blacklisted (true/false).
The system uses logical operators to evaluate her access eligibility:
If she is registered AND has a valid ID, and NOT blacklisted, she is granted access.
Otherwise, access is denied.
Your task is to evaluate these conditions using logical operators and print whether access is granted or denied.
Input Format:
Three boolean values entered by the user (true or false):
<isRegistered>
<hasValidID>
<isBlacklisted>
Output Format:
Access Granted: true/false
For example:
Input	Result
true
true
false
Access Granted: true
```

## AIM:
To evaluate access eligibility using logical operators based on registration, valid ID, and blacklist status.

## ALGORITHM :
1, Begin the program and create a Scanner object to read user input.
2, Accept three boolean values for registration, valid ID, and blacklist status.
3, Store these inputs in separate boolean variables.
4, Apply the logical expression (isRegistered && hasValidID && !isBlacklisted) to evaluate access.
5, Print whether access is granted based on the logical result.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by:  SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;
public class java{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        boolean a=sc.nextBoolean();
        boolean b=sc.nextBoolean();
        boolean c=sc.nextBoolean();
        System.out.println("Access Granted: "+(a && b && !c));
    }
}
```

## OUTPUT:
<img width="578" height="235" alt="image" src="https://github.com/user-attachments/assets/6948c52f-187b-4f73-b304-57acee01ca7d" />

## RESULT:
Thus, the program was successfully executed to check access eligibility using logical operators, and it correctly displayed whether access is granted based on the given boolean inputs.



