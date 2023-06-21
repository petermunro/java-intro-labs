# Creating ("Instantiating") Objects in Java

These exercises focus on instantiating objects from the `java.lang` package. They don't require you to create new classes.

1. Create a new class.

2. Create a `main` method within that class. Perform the operations below in this main method.

3. Instantiate a new `String` object with the text "Hello, world!". Assign it to a variable of type `String`.

4. Instantiate a new `int` _primitive_ with the value **42**. Assign it to a variable of type `int`.

5. Instantiate a new `double` _primitive_ with the value **3.14**. Assign it to a variable of type `double`.

6. Instantiate a new `boolean` _primitive_ with the value **true**. Assign it to a variable of type `boolean`.

7. Instantiate a new `char` _primitive_ with the value **'a'**. Assign it to a variable of type `char`.

8. Instantiate a new `Integer` _object_ with the value **43**. Assign it to a variable of type `Integer`.

## Using classes from other packages

The `Random` class is in the `java.util` package. So you'll need to import `java.util.Random` before using it.

1. Instantiate a new `Random` _object_. You can do this by simply calling the `Random()` constructor with no arguments, like this:

   ```java
   Random random = new Random();
   ```

2. Use the `nextInt()` method on the `Random` object to generate a random integer between 0 and 10. Assign it to a variable of type `int`, like this:

   ```java
   int randomInt = random.nextInt(11);
   ```

   This will generate a random integer between 0 and 10 (inclusive) and assign it to the variable `randomInt`.

   Print out the random integer. Verify that you get a different one each time you run the program.
