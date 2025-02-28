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