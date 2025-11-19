# Ex.No:3(D)    INTERFACE 

## QUESTION:
You're building the equalizer system for a music app like BeatBoxx. The equalizer has 3 basic sound modes:
BassBoost
VocalBoost
Balanced
Each mode behaves differently and alters the sound experience. The app uses a SoundMode interface that each mode implements.

## AIM:
To develop an equalizer system for a music app using interfaces in Java.
The system should allow users to select one of three sound modes — BassBoost, VocalBoost, or Balanced — and apply the corresponding audio settings.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Use a switch case to check which mode the user selected.
4. Create an object of the corresponding class (BassBoost, VocalBoost, or Balanced) using the SoundMode interface.
5. Call the applySettings() method, which executes the overridden version based on the selected mode.
6. Display the output message, showing which sound effect has been applied.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

interface SoundMode {
    void applySettings();
}

class BassBoost implements SoundMode {
    public void applySettings() {
        System.out.println("Bass Boost applied. Feel the beat drop!");
    }
}

class VocalBoost implements SoundMode {
    public void applySettings() {
        System.out.println("Vocal Boost enabled. Enjoy crystal-clear lyrics!");
    }
}

class Balanced implements SoundMode {
    public void applySettings() {
        System.out.println("Balanced mode set. A perfect blend of bass and vocals.");
    }
}

public class BeatBoxxEqualizer {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String mode = sc.nextLine().trim().toLowerCase();

        SoundMode soundMode;

        switch (mode) {
            case "bass":
                soundMode = new BassBoost();
                break;
            case "vocal":
                soundMode = new VocalBoost();
                break;
            case "balanced":
                soundMode = new Balanced();
                break;
            default:
                System.out.println("Invalid mode selected.");
                sc.close();
                return;
        }

        soundMode.applySettings();
        sc.close();
    }
}

```


## OUTPUT:

<img width="1090" height="160" alt="image" src="https://github.com/user-attachments/assets/112f2e68-d2b5-438e-9579-83d7f9dca52e" />


## RESULT:
Thus, the program successfully implemented abstraction using the SoundMode interface and demonstrated runtime polymorphism by applying different equalizer settings through BassBoost, VocalBoost, and Balanced classes. The selected mode produced the correct audio setting message based on user input.

