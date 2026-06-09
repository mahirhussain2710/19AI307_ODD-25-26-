# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

Input Format:

n [Player1] [Player2] ... First line: Integer n – number of players turning on consoles

Next n lines: Each line contains the player's name.

Output Format: For each player, print:

[PlayerName] accessed Master Power Switch. Total accesses so far: [count]

For example:

Input Result 3 Alice Bob Charlie Alice accessed Master Power Switch. Total accesses so far: 1 Bob accessed Master Power Switch. Total accesses so far: 2 Charlie accessed Master Power Switch. Total accesses so far: 3 1 Zara Zara accessed Master Power Switch. Total accesses so far: 1

## AIM:
To develop a Java program demonstrating the Singleton design pattern with shared state management.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with a private static instance.
4. Define a private constructor.
5. Provide a public static method to access the instance.
6. Maintain a static counter variable.
7. Increment count on each access.
8. Read input values.
9. Call the Singleton instance method.
10.Display the result.
11.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

// Singleton Class
class MasterPowerSwitch {

    // Step 1: Create a private static instance
    private static MasterPowerSwitch instance;

    // Step 2: Create a private constructor
    private MasterPowerSwitch() {
    }

    // Step 3: Global access point
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    // Access counter
    private int accessCount = 0;

    public int accessSwitch() {
        accessCount++;
        return accessCount;
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = Integer.parseInt(sc.nextLine());

        MasterPowerSwitch masterSwitch = MasterPowerSwitch.getInstance();

        for (int i = 0; i < n; i++) {
            String playerName = sc.nextLine();
            int count = masterSwitch.accessSwitch();

            System.out.println(playerName + 
                " accessed Master Power Switch. Total accesses so far: " + count);
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1256" height="327" alt="image" src="https://github.com/user-attachments/assets/4215dece-4dac-4a76-96e7-229ddcedbc52" />


## RESULT:
The program was executed successfully and demonstrated the Singleton pattern with shared access count.
