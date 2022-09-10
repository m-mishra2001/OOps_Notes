# Static Keyword

The static keyword in Java is mainly used for memory management.
The static keyword is a non-access modifier in Java that is applicable for the following: 

Blocks

Variables

Methods

Classes

## Static Variable

![image](https://user-images.githubusercontent.com/60498472/189468902-ead33a16-0eba-47a6-9ea6-d8bc3d0b68a4.png)

![image](https://user-images.githubusercontent.com/60498472/189468910-cf67ac50-b50b-467f-801e-9bbb6eafdffb.png)

Note:- A static variable can only be declared inside main public class or inside a static block or method. if we 
try to declare tstaic variable inside non static member of class then java prompt compilation error.

## Static Methods

![image](https://user-images.githubusercontent.com/60498472/189469144-6a299c01-eadd-404e-addb-af5b27fb7039.png)

``` java 

// Java program to demonstrate restriction on static methods
  
class Test
{
    // static variable
    static int a = 10;
      
    // instance variable
    int b = 20;
      
    // static method
    static void m1()
    {
        a = 20;
        System.out.println("from m1");
          
         // Cannot make a static reference to the non-static field b
         b = 10; // compilation error
                  
         // Cannot make a static reference to the 
                 // non-static method m2() from the type Test
         m2();  // compilation error
           
         //  Cannot use super in a static context
         System.out.println(super.a); // compiler error 
    }
      
    // instance method
    void m2()
    {    
        System.out.println("from m2");
    }
      
      
      
    public static void main(String[] args)
    {
        // main method 
    }
}
```

## Static Block

If you need to do the computation in order to initialize your static variables, you can declare a static block that gets executed exactly once, when the class is first loaded. 
A static block executed  at the begining before main() mathod  and constructor .

![image](https://user-images.githubusercontent.com/60498472/189469329-66672547-7b55-4bb4-86e3-8b30a1751bc9.png)

![image](https://user-images.githubusercontent.com/60498472/189469331-970b2a06-a13c-4d5c-bdc7-d6e382b5f82e.png)

```java
 static {
        System.out.println("Static block initialized.");
        b = a * 4;
    }
```

## Static class

 
A class can be made static only if it is a nested class. We cannot declare a top-level class with a static modifier but can declare nested classes as static. Such types of classes are called Nested static classes. Nested static class doesn’t need a reference of Outer class. In this case, a static class cannot access non-static members of the Outer class. 

``` java

// A java program to demonstrate use
// of static keyword with Classes
  
import java.io.*;
  
public class GFG {
  
    private static String str = "GeeksforGeeks";
  
    // Static class
    static class MyNestedClass {
        
        // non-static method
        public void disp(){ 
          System.out.println(str); 
        }
    }
    
    public static void main(String args[])
    {
        GFG.MyNestedClass obj
            = new GFG.MyNestedClass();
        obj.disp();
    }
}
```

# when to use Static Variable and Methods
Use the static variable for the property that is common to all objects. For example, in class Student, all students share the same college name. Use static methods for changing static variables.
