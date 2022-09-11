# Abstract 
- Abstract Class 

- Abstract Methods

![image](https://user-images.githubusercontent.com/60498472/189511681-925c461f-ed62-472a-adfd-cf6be3b21b90.png)


![image](https://user-images.githubusercontent.com/60498472/189511687-4d0ceee2-5976-4117-b10a-97a6b0f8c1fa.png)


![image](https://user-images.githubusercontent.com/60498472/189511754-61df15f1-2b77-497d-a156-6cfd94c0f45a.png)

``` java

public abstract class Employee {
   private String name;
   private String address;
   private int number;

   public abstract double computePay();
   // Remainder of class definition
}
```

# Final 
The final keyword in java is used to restrict the user. The java final keyword can be used in many context. Final can be:

variable
method
class
The final keyword can be applied with the variables, a final variable that have no value it is called blank final variable or uninitialized final variable. It can be initialized in the constructor only. The blank final variable can be static also which will be initialized in the static block only

- Java final variable
If you make any variable as final, you cannot change the value of final variable(It will be constant).

``` java
class Bike9{  
 final int speedlimit=90;//final variable  
 void run(){  
  speedlimit=400;  
 }  
 public static void main(String args[]){  
 Bike9 obj=new  Bike9();  
 obj.run();  
 }  
}//end of class  
```

- Java final method

If you make any method as final, you cannot override it.

``` java
class Bike{  
  final void run(){System.out.println("running");}  
}  
     
class Honda extends Bike{  
   void run(){System.out.println("running safely with 100kmph");}  
     
   public static void main(String args[]){  
   Honda honda= new Honda();  
   honda.run();  
   }  
}  ```


- Java final class

If you make any class as final, you cannot extend it.

``` java
final class Bike{}  
  
class Honda1 extends Bike{  
  void run(){System.out.println("running safely with 100kmph");}  
    
  public static void main(String args[]){  
  Honda1 honda= new Honda1();  
  honda.run();  
  }  
}  
```


# [this Keyword](https://www.javatpoint.com/this-keyword)

# [new Keyword](https://www.javatpoint.com/new-keyword-in-java)

# [Super Keyword](https://www.javatpoint.com/super-keyword)
