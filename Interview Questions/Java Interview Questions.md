1. Predict the output :
```
class A {
    static void foo() {
        System.out.println("A");
    }
}

class B extends A {
    static void foo() {
        System.out.println("B");
    }
}

public class Test {
    public static void main(String[] args) {
        A obj = new B();
        obj.foo();
    }
}
```
2. Predict the output :
```
class Parent {
    Parent() {
        init();
    }

    void init() {
        System.out.println("Parent init");
    }
}

class Child extends Parent {
    int x = 10;

    Child() {
        System.out.println("Child constructor");
    }

    @Override
    void init() {
        System.out.println("Child init, x = " + x);
    }
}

public class Test {
    public static void main(String[] args) {
        new Child();
    }
}
```
3. Predict the output :
```
class Test {
    public static void main(String[] args) {
        System.out.println(10 + 20 + "30" + 40 + 50);
    }
}
```
4. Predict the output :
```
Integer a = 128;
Integer b = 128;

System.out.println(a == b);
System.out.println(a.equals(b));
```
5. State the possible output range and the exact JVM-level reason it is not deterministic.
```
class Counter {
    int count = 0;

    void increment() {
        count++;
    }
}

public class Test {
    public static void main(String[] args) throws Exception {
        Counter c = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1_000_000; i++) c.increment();
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1_000_000; i++) c.increment();
        });

        t1.start();
        t2.start();
        t1.join();
        t2.join();

        System.out.println(c.count);
    }
}
```
6. Predict the output :
```
public class Test {
    public static void main(String[] args) {
        String s1 = "hello";
        String s2 = "hello";
        String s3 = new String("hello");

        System.out.println(s1 == s2);
        System.out.println(s1 == s3);
        System.out.println(s1.equals(s3));
    }
}
```
7. Explain the difference between Stack memory and Heap memory in Java, including lifetime, thread visibility, and what actually causes a `StackOverflowError` vs an `OutOfMemoryError`.
8. 
