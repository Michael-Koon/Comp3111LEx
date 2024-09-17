# Lab 2

KOON, Tsz Hin

20776071

## Part 1: `Book.java`

```java
package Lab2b;

/*	Comp3111LEx\Lab2b\Book.java		*/
public class Book {
    private String chapters[];
    private static final int DEFAULT_CHAPTERS = 10;

    public Book() {
        chapters = new String[DEFAULT_CHAPTERS];
        for (int i = 0; i < chapters.length; i++)
            chapters[i] = "n/a";
    }
    public Book(String argument[]) {
        /* construct the object with an array of chapter names */
        /* PLEASE ADD YOUR CODE HERE */
        chapters = argument;
    }
    public String getChapter(int i) {
        /* return the chapter by the given index */
        /* PLEASE ADD YOUR CODE HERE */
        return chapters[i];
    }
    public String[] getChapters() {
        return chapters;
    }
}
```

## Part2: `MobileComputer.java`

```java
package Lab2c;

/*	Comp3111LEx\Lab2c\MobileComputer.java
	Inherits from Computer, class library for Lab2 Exercise 3	*/

public class MobileComputer extends Computer implements Chargeable {
    private int battery;
    public MobileComputer() {
        secret = "MobileComputer secret";
        battery = 5;
    }
    @Override
    public void work() {
        if (battery > 0) {
            System.out.println("It is working on my lap.");
            battery--;
        } else
            System.out.println("Running out of battery");
    }
    @Override
    public void charge() {
        if (battery < 10)
            battery++;
    }
}
```

Explanation:

`Chargeable` was not implemented in `MobileComputer`, add `implements` and `@Override` to `charge()` in order to use the `Chareable`.
