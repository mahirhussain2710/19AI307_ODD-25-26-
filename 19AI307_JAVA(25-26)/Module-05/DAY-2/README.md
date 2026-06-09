# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList) into a file.

Input Result 2 101 Alice 89.5 102 Bob 92.0 Students serialized successfully into: students.dat Students deserialized successfully from: students.dat

Deserialized Students: Student{id=101, name='Alice', marks=89.5} Student{id=102, name='Bob', marks=92.0}

## AIM:
To develop a Java program demonstrating object serialization and deserialization using file handling.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class implementing Serializable.
4. Create a collection of objects.
5. Write objects to a file using ObjectOutputStream.
6. Read objects from file using ObjectInputStream.
7. Display the deserialized data.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    int id;
    String name;
    double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class Main {

    @SuppressWarnings("unchecked") // removes unchecked warning
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Student> students = new ArrayList<>();

        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            int id = sc.nextInt();
            sc.nextLine(); // consume newline
            String name = sc.nextLine();
            double marks = sc.nextDouble();

            students.add(new Student(id, name, marks));
        }

        String filename = "students.dat";

        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + filename);
        } catch (IOException e) {
            System.out.println("Serialization error: " + e.getMessage());
        }

        ArrayList<Student> deserializedStudents = null;

        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename))) {
            deserializedStudents = (ArrayList<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + filename);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Deserialization error: " + e.getMessage());
        }

        System.out.println("\nDeserialized Students:");
        if (deserializedStudents != null) {
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1265" height="466" alt="image" src="https://github.com/user-attachments/assets/7d5a2836-ec6e-478c-92ad-5c231b36edc5" />

## RESULT:
The program was executed successfully and demonstrated serialization and deserialization of objects.
