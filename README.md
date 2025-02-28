# Balon and Bayles - REPORT

---

## JAVA Inner Classes

In Java, it is also possible to nest classes (a class within a class).An inner class is a class defined within another class. 

The purpose of nested classes is to group classes that belong together, which makes your code more readable and maintainable.

### Example:

```java
class OuterClass {
  int x = 10;

  class InnerClass {
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}
```
```code
Output: 15 (5 + 10)
```

A default (non-static) inner class is a class declared inside another class without the static keyword.

### Purpose & Value
- Used when the inner class needs access to the outer class’s instance members.
- Commonly used in scenarios where a class is only relevant within another class.

### Example:
```java
class Outer {
    class Inner {  // Default (Non-static) Inner Class
        void display() {
            System.out.println("Inside Inner Class");
        }
    }

    void createInner() {
        Inner inner = new Inner();  // Creating an inner class instance
        inner.display();
    }
}

public class Main {
    public static void main(String[] args) {
        Outer outer = new Outer();
        outer.createInner();

        // Alternatively, we can create an Inner class instance from outside:
        Outer.Inner innerObj = outer.new Inner();
        innerObj.display();
    }
}
```
### Key Points
- Requires an instance of the outer class to be created.
- Can access private members of the outer class.

---

## Private Inner Class

A private inner class is a non-static inner class marked as private.

Unlike a "regular" class, an inner class can be private or protected. If you don't want outside objects to access the inner class, declare the class as private.

Purpose & Value
Used when the inner class is meant to be hidden from external access.
Ensures tight encapsulation.

### Example:
```java
class OuterClass {
  int x = 10;

  private class InnerClass {
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}
```

If you try to access a private inner class from an outside class, an error occurs:

```error
Main.java:13: error: OuterClass.InnerClass has private access in OuterClass
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
              ^
```

### Example:
```java
class Outer {
    private class Inner {  // Private Inner Class
        void show() {
            System.out.println("Inside Private Inner Class");
        }
    }

    void accessInner() {
        Inner inner = new Inner();
        inner.show();
    }
}

public class Main {
    public static void main(String[] args) {
        Outer outer = new Outer();
        outer.accessInner();  // Works fine

        // Outer.Inner inner = outer.new Inner(); // Error: Inner is private
    }
}

```

### Key Points
- Cannot be accessed from outside the outer class.
- The outer class needs to provide a public method to interact with the private inner class.

---

## Static Inner Class (Nested Static Class)

An inner class can also be static, which means that you can access it without creating an object of the outer class.

### Purpose & Value
- Used when the inner class does not need access to instance members of the outer class.
- Can be instantiated without creating an instance of the outer class.
- Useful in utility/helper classes.

### Example:
```java
class Outer {
    static class Inner {  // Static Inner Class
        void show() {
            System.out.println("Inside Static Inner Class");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Outer.Inner inner = new Outer.Inner();  // No need for Outer instance
        inner.show();
    }
}
```

### Key Points
- Can be accessed without an instance of the outer class.
- Cannot access non-static members of the outer class.



