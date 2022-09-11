# Polymorphism
Polymorphism in Java is a concept by which we can perform a single action in different ways. Polymorphism is derived from 2 Greek words: poly and morphs. The word "poly" means many and "morphs" means forms. So polymorphism means many forms.

There are two types of polymorphism in Java: 
- compile-time polymorphism
- runtime polymorphism.

## Type 1: Compile-time polymorphism

It is also known as static polymorphism. This type of polymorphism is achieved by function overloading or operator overloading. 

Method Overloading: When there are multiple functions with the same name but different parameters then these functions are said to be overloaded. 
Functions can be overloaded by change in the number of arguments or/and a change in the type of arguments.
Note :- java does not support operator overloading
 
## Runtime Polymorphism in Java
Runtime polymorphism or Dynamic Method Dispatch is a process in which a call to an overridden method is resolved at runtime rather than compile-time.
n this process, an overridden method is called through the reference variable of a superclass. The determination of the method to be called is based on the object being referred to by the reference variable.

Let's first understand the upcasting before Runtime Polymorphism.

Upcasting
If the reference variable of Parent class refers to the object of Child class, it is known as upcasting. For example:

![image](https://user-images.githubusercontent.com/60498472/189525923-2383dab0-183c-4f4b-9ff6-46bca712a489.png)

``` java
Upcasting in Java
class A{}  
class B extends A{}  
A a=new B();//upcasting  
For upcasting, we can use the reference variable of class type or an interface type. For Example:

interface I{}  
class A{}  
class B extends A implements I{}  ```


### Example of Java Runtime Polymorphism
In this example, we are creating two classes Bike and Splendor. Splendor class extends Bike class and overrides its run() method. We are calling the run method by the reference variable of Parent class. Since it refers to the subclass object and subclass method overrides the Parent class method, the subclass method is invoked at runtime.

Since method invocation is determined by the JVM not compiler, it is known as runtime polymorphism

``` java
class Bike{  
  void run(){System.out.println("running");}  
}  
class Splendor extends Bike{  
  void run(){System.out.println("running safely with 60km");}  
  
  public static void main(String args[]){  
    Bike b = new Splendor();//upcasting  
    b.run();  
  }  
}  
```
