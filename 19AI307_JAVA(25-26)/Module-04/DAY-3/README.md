# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

For example:
Input Result 2 Java James Gosling Python Guido Van Rossum Books in Library:
Java by James Gosling
Python by Guido Van Rossum 1 Machine Learning Andrew Ng Books in Library:
Machine Learning by Andrew Ng

## AIM:
To develop a Java program demonstrating composition where objects are created and managed within another class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class representing a container.
4. Create another class representing contained objects.
5. Instantiate contained objects within the container class.
6. Read input values.
7. Store objects inside the container.
8. Display stored object details.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;

class Library {

    private class Book {
        private String title;
        private String author;

        public Book(String title, String author) {
            this.title = title;
            this.author = author;
        }

        public void display() {
            System.out.println("- " + title + " by " + author);
        }
    }

    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        Book book = new Book(title, author); // Created inside Library
        books.add(book);
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book book : books) {
            book.display();
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Library library = new Library();

        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();

        sc.close();
    }
}
```


## OUTPUT:
<img width="1165" height="672" alt="image" src="https://github.com/user-attachments/assets/335e60fa-586d-42d7-a36e-364dffdb71e3" />

## RESULT:
The program was executed successfully and demonstrated composition with proper object management.
