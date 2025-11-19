# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To implement the Abstract Factory pattern for generating Button and Checkbox UI components based on the selected theme (dark or light).

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define product interfaces Button and Checkbox to represent UI components.
4. Create dark and light theme product classes implementing these interfaces.
5. Define a UIFactory interface declaring methods to create themed components.
6. Implement DarkThemeFactory and LightThemeFactory to generate the corresponding products.
7. Read user input (dark/light), create the appropriate factory, and generate Button & Checkbox through it.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
import java.util.Scanner;

// Product interfaces
interface Button {
    void create();
}

interface Checkbox {
    void create();
}

// Dark theme products
class DarkButton implements Button {
    public void create() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void create() {
        System.out.println("Dark Checkbox created");
    }
}

// Light theme products
class LightButton implements Button {
    public void create() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void create() {
        System.out.println("Light Checkbox created");
    }
}

// Abstract factory
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// Concrete factories
class DarkThemeFactory implements UIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();

        UIFactory factory;

        if (theme.equals("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equals("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            return;
        }

        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();

        button.create();
        checkbox.create();
    }
}

```


## OUTPUT:

<img width="646" height="273" alt="image" src="https://github.com/user-attachments/assets/fad6eee5-5174-4dbb-a0e9-76af3ef82a6b" />


## RESULT:
The program successfully generates theme-specific Button and Checkbox components using the Abstract Factory pattern.
