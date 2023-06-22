**Exercise: Writing to a file in Java using FileWriter with try-with-resources**

**Part 1: Write to a File**
Let's write something to a file:

```java
import java.io.FileWriter;   // Import the FileWriter class
import java.io.IOException;  // Import the IOException class to handle errors

public class Main {
  public static void main(String[] args) {
    try (FileWriter myWriter = new FileWriter("filename.txt")) {
      myWriter.write("Files in Java might be tricky, but it is fun enough!");
      System.out.println("Successfully wrote to the file.");
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```

Notice that don't need to manually close the `FileWriter`. With the try-with-resources statement, it gets automatically closed when the program finishes with it.

**Part 2: Write Multiple Lines to the File**
Next, let's write multiple lines to the file. Again, replace the body of your `main` method with the following:

```java
import java.io.FileWriter;   // Import the FileWriter class
import java.io.IOException;  // Import the IOException class to handle errors

public class Main {
  public static void main(String[] args) {
    try (FileWriter myWriter = new FileWriter("filename.txt")) {
      myWriter.write("Files in Java might be tricky, but it is fun enough!\n");
      myWriter.write("Here is another line.");
      System.out.println("Successfully wrote to the file.");
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```

**Part 3: Appending to the File**

Let's now append to the file instead of overwriting it. Replace the body of your `main` method with the following:

```java
import java.io.FileWriter;   // Import the FileWriter class
import java.io.IOException;  // Import the IOException class to handle errors

public class Main {
  public static void main(String[] args) {
    try (FileWriter myWriter = new FileWriter("filename.txt", true)) {
      myWriter.write("\nWriting to a file in Java can be easy!");
      System.out.println("Successfully wrote to the file.");
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```

**Part 4: Using BufferedWriter with try-with-resources**

Finally, let's use BufferedWriter with try-with-resources. Again, replace the body of your `main` method with the following:

```java
import java.io.FileWriter;   // Import the FileWriter class
import java.io.BufferedWriter; // Import the BufferedWriter class
import java.io.IOException;  // Import the IOException class to handle errors

public class Main {
  public static void main(String[] args) {


    try (FileWriter myWriter = new FileWriter("filename.txt", true);
         BufferedWriter bufferedWriter = new BufferedWriter(myWriter)) {

      bufferedWriter.write("\nBufferedWriter can increase writing efficiency!");
      bufferedWriter.newLine();
      bufferedWriter.write("It writes text to a character-output stream, buffering characters to provide efficient writing.");

      System.out.println("Successfully wrote to the file.");

    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```

Using `try-with-resources` is generally preferred because it automatically closes resources when they are no longer needed. This reduces the risk of resource leaks and makes your code cleaner and easier to read.
