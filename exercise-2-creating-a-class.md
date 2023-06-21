# Creating a class in Java

This exercise involves instantiating a Person object:

1. Open your Java development environment. This could be an IDE like Eclipse or IntelliJ, or you could use a text editor like Visual Studio Code and compile and run your code from the command line.
2. Create a new Java file called `Person.java`. You can do this from the command line or from within your IDE.
3. In the `Person` class, create two instance variables:

   - name, and
   - age

   You can do this by declaring two variables with appropriate data types, like this:

   ```java
   public class Person {
     String name;
     int age;
   }
   ```

4. Create a `main` method in your class.

5. In the main method, instantiate a Person object. You can do this by using the `new` keyword followed by the name of the class and parentheses, like this:

   ```java
   Person person1 = new Person();
   ```

   This creates a new `Person` object and assigns it to the variable `person1`.

6. Assign values to the `name` and `age` instance variables of the `Person` object you just instantiated. You can do this by using the dot notation, like this:

   ```java
   person1.name = "Alice";
   person1.age = 25;
   ```

   This sets the `name` instance variable of `person1` to "Alice" and the `age` instance variable to 25.

7. Print out the values of the `name` and `age` instance variables to make sure they were set correctly. You can do this by using the `System.out.println()` method, like this:

   ```java
   System.out.println("Name: " + person1.name);
   System.out.println("Age: " + person1.age);
   ```

   This will print out the values of `person1` and `age` instance variables to the console.

8. Compile and run your Java file to see the output. If everything was done correctly, you should see the name and age of the Person object you created printed to the console!

That's it! By following these steps, you should be able to successfully instantiate a `Person` object in Java and assign values to its instance variables.
