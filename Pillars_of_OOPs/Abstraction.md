# Abstraction

## [Abstract class and Abstract Method](https://github.com/m-mishra2001/OOps_Notes/blob/main/Pillars_of_OOPs/Important%20Keywords/KeyWords_this_super_etc.md)

![image](https://user-images.githubusercontent.com/60498472/189526958-a518d5b7-69ca-42b0-a8b3-e3b8128e578f.png)



- Why object can not be created for an abstract class though it contains a constructor?

you can't create a object of abstract class because there is an abstract method which has nothing so you can call that abstract method too.
If we will create an object of the abstract class and calls the method having no body(as the method is pure virtual) it will give an error.

- The abstract class can also be used to provide some implementation of the interface
. In such case, the end user may not be forced to override all the methods of the interface.

```java
interface A{  
void a();  
void b();  
void c();  
void d();  
}  
  
abstract class B implements A{  
public void c(){System.out.println("I am c");}  
}  
  
class M extends B{  
public void a(){System.out.println("I am a");}  
public void b(){System.out.println("I am b");}  
public void d(){System.out.println("I am d");}  
}  
  
class Test5{  
public static void main(String args[]){  
A a=new M();  
a.a();  
a.b();  
a.c();  
a.d();  
}}  
```

## When to use Abstraction

The main purpose of abstraction is hiding the unnecessary details from the users. Abstraction is selecting data from a larger pool to show only relevant details of the object to the user. It helps in reducing programming complexity and efforts.

# Interfaces
An interface in Java is a blueprint of a class.

Interfaces specify what a class must do and not how. It is the blueprint of the class.

If a class implements an interface and does not provide method bodies for all functions specified in the interface, then the class must be declared abstract.

- Why do we use an Interface?
It is used to achieve total abstraction.

Since java does not support multiple inheritances in the case of class, by using an interface it can achieve multiple inheritances.

It is also used to achieve loose coupling.
[Loose coupling](https://www.javatpoint.com/loose-coupling-in-java#:~:text=To%20achieve%20loose%20coupling%2C%20one,will%20make%20the%20concept%20clearer.)


Interfaces are used to implement abstraction. So the question arises why use interfaces when we have abstract classes?

The reason is, abstract classes may contain non-final variables, whereas variables in the interface are final, public and static.

# [Differentiate between abstract class and Interface](https://www.javatpoint.com/difference-between-abstract-class-and-interface)

