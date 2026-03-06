# Java Programming Basics
#### Basic fundamentals of Java programming

## Contents:
- Variables
- I/O
- Operators
- Conditional Statements
- Selection Statements
- Loops

---

## Variables

A variable is a named reference to a value stored in memory.
It allows programs to store, access, and modify data during execution.

A variable in Java has three components:
- Data Type - What kind of data is stored.
- Variable Name - A unique identifier following Java naming rules.
- Value - The data assigned to the variable.

Example:
```java
int var = 10;
```
Here:
- int - Data Type
- var - Variable Name
- 10 - Value

---

## Variable Scope

Variables can be catagorized based on where they are declared and where they can be accessed.

### Local Variables

Local variables are declared inside a specific block, such as a function or loop.
These can only be accessed within the block where they are declared.
Once the scope ends, the variable becomes inaccessible and may be removed from memory.

Example:
```java
public class Main {
    public static void func() {
        String local_var = "I am a local variable";
        System.out.println(local_var);
    }

    public static void main(String[] args) {
        func();
    }
}
```

---

### Global Variables

Global variables are declared outside a function or block, usually at the beginning at the top or in a separate file.
These can be accessed from most parts of the program such as functions, loops, or classes.
Global variables retain their value throughout the program unless modified by some operator.

Example:
```java
public class Main {
    static String global_var = "I am a global variable";

    public static void func() {
        System.out.println(global_var);
    }
    public static void main(String[] args) {
        func();
        System.out.println(global_var);
    }
}
```
Notice how `global_var` is accessed inside `func()` and `main()`.
