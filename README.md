This Java code performs a recursive operation to visit files and directories within a specified starting directory. Here's a detailed explanation of the code:

1. Importing necessary libraries: The code imports required classes from `java.io.IOException`, `java.nio.file.*`, and `java.nio.file.attribute.BasicFileAttributes`.

2. Definition of the main class `Main`: The main class `Main` contains the `main` method, which is the entry point of the program.

3. Creating the starting path: An object `Path` named `startingPath` is created, representing the starting directory for the visit operation.

4. Creating a `StatsVisitor` object: An instance of `StatsVisitor` is instantiated, which is an inner class within the `Main` class and extends `SimpleFileVisitor<Path>`. This class will be used to define the behavior of file and directory visitation.

5. Executing the file and directory visitation: The `walkFileTree` method of the `Files` class is invoked, passing the starting path (`startingPath`) and the `StatsVisitor` object as the visitor. This method performs the recursive visitation of files and directories.

6. Handling exceptions: Any `IOException` that occurs during the visit operation is caught, and a new `RuntimeException` is thrown to terminate the program.

7. Definition of the inner class `StatsVisitor`: This class extends `SimpleFileVisitor<Path>` and provides methods to handle file and directory visitation.

   - The `visitFile` method is called for each visited file and prints the file's name.
   - The `preVisitDirectory` method is called before visiting a directory and prints the directory's name.
   - The `postVisitDirectory` method is called after visiting a directory and decrements the current level.

In summary, this code performs a recursive visitation of files and directories within a starting directory and prints their names during the visit operation.
