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
2. 
