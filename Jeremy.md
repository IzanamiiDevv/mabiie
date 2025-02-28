### **What is a Java Method?**  
A **Java method** is a block of code within a class that performs a specific task. Methods help in code reusability, modularity, and organization, making programs more efficient and readable.

---

### **Key Features of Java Methods**  
1. **Encapsulation of Logic** – A method groups related operations together.  
2. **Code Reusability** – You can call a method multiple times without rewriting the same code.  
3. **Parameterization** – Methods can take input values (parameters) to process different data.  
4. **Return Values** – Methods can return results to the caller.  

---

### **Types of Java Methods**  

1. **Predefined Methods (Built-in Methods)**  
   - These are provided by Java libraries, such as `Math.pow()`, `System.out.println()`, etc.  

2. **User-Defined Methods**  
   - Created by programmers to perform specific tasks.

3. **Static Methods**  
   - Declared using `static`, can be called without creating an object.  

4. **Instance Methods**  
   - Requires an object of the class to be called.

---

### **Basic Java Method Example**
```java
class Example {
    // User-defined method
    public void greet() {
        System.out.println("Hello, welcome to Java!");
    }

    public static void main(String[] args) {
        Example obj = new Example(); // Creating an object
        obj.greet(); // Calling the method
    }
}
```
**Output:**  
```
Hello, welcome to Java!
```

Would you like examples of different types of methods?