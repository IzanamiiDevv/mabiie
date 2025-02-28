# Java Class Method.

In Java, a method is a block of code that performs a specific task. It is defined inside a class and can be called to execute the code within it.

## **Key Features of Java Methods**  
1. **Encapsulation of Logic** – A method groups related operations together.  
2. **Code Reusability** – You can call a method multiple times without rewriting the same code.  
3. **Parameterization** – Methods can take input values (parameters) to process different data.  
4. **Return Values** – Methods can return results to the caller.  

## **Syntax:**
```java
modifiers return-type method-name(parameter-list) {
    // Method body
    return value; // (if the return type is not void)
}
```
- **modifiers** (optional): Defines the access level (`public`, `private`, `protected`) or method properties (`static`, `final`).
- **return-type**: Specifies the data type of the returned value (`int`, `void`, `String`, etc.).
- **method-name**: The name of the method (should follow camelCase convention).
- **parameter-list** (optional): Input values required for the method.
- **method body**: Contains the logic/code to be executed.
- **return value** (if applicable): Returns a result if the return type is not `void`.

### **Example: Creating and Using a Java Method**
```java
class MyClass {
    // Method to add two numbers and return the result
    public int addNumbers(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        MyClass obj = new MyClass();  // Creating an object of MyClass
        int sum = obj.addNumbers(5, 10);  // Calling the method
        System.out.println("Sum: " + sum);  // Output: Sum: 15
    }
}
```

#### **Explanation:**
1. `public int addNumbers(int a, int b)`: A method that takes two integers and returns their sum.
2. `MyClass obj = new MyClass();`: Creating an instance of the class.
3. `int sum = obj.addNumbers(5, 10);`: Calling the method and storing the result.
4. `System.out.println("Sum: " + sum);`: Printing the output.