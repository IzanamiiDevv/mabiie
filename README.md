# JAVA Inner Classes

In Java, it is also possible to nest classes (a class within a class).An inner class is a class defined within another class. 

The purpose of nested classes is to group classes that belong together, which makes your code more readable and maintainable.


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

---