# Java


1. Ensure that you are inside the Java and complete directory .
To execute JRE to class
``` bash
javac Welcome.java
```

To eceute the class from Javac
``` bash
java Welcome
```
Use CMD
To ensure the version of your application
``` bash
java -version
```

Ensure that it is capital letters.
This is an example of executable code in Java
``` bash
public class Welcome {

public static void main(String[] args) {
    System.out.println("Welcome Kirstenumali");
  }
}
```







**Java Memory Management: Garbage Collection, JVM Tuning, and Spotting Memory Leaks (Garbage Collector)**
``` bash
java Example
java -Xmx1024m Example
java -Xmx10m Example
java -XX:MaxNewSzie=128m Example
java -XX:MaxMetaSpaceSize=4 Example
```
``` bash
package com.enrollmentsystem.pro;

import java.util.ArrayList;

public class Example {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<Integer>();
        int i = 0;
        while(true) {
            list.add(Integer.valueOf(3));
            if (i>1000) {
                list = new ArrayList<>();
                i =0;
            }
            i++;
        }
    }
}
```


# What are Object-Oriented-Programming Concepts in Java
Object-Oriented Programming (OOP) concepts in Java. We’ll discuss classes, objects, abstraction, encapsulation, inheritance, and polymorphism.

Classes - are the starting point of all objects, and we may consider them as the template for creating objects. Class includes member fields, methods, and special constructor. 


// Class. For example:
public class Car {
 
    // member fields
    private String type;
    private String model;
    private String color;
    private int speed;
 
    // constructor
    public Car(String type, String model, String color) {
        this.type = type;
        this.model = model;
        this.color = color;
    }
     
    // member methods
    public int increaseSpeed(int increment) {
        this.speed = this.speed + increment;
        return this.speed;
    }
     
    // ...
}

Objects or instances of the class - We create objects from classes using their constructors.

// Objects or instance of the class. For example:

Car veyron = new Car("Bugatti", "Veyron", "crimson");
Car corvette = new Car("Chevrolet", "Corvette", "black");

Here, we’ve created two instances of the class Car. 
In other words, objects are also called instances of the class of the class Car.


Abstraction - concealing implementation complexity and revealing more straightforward interfaces.
In OOP, abstraction means hiding the complex implementation details of a program.
Abstraction - hiding the complex implementation details

Encapsulation - is hiding the state or internal representation of an object from the consumer of an API
Encapsulation - hiding the state or internal representation


// Encapsulation. For example: 
public class Car {

    // ...
    private int speed;

    public int getSpeed() {
        return color;
    }

    public void setSpeed(int speed) {
        this.speed = speed;
    }
    // ...
}

Here, the field speed is encapsulated using the private access modifier, and can only be accessed using the public getSpeed() and setSpeed() methods. 




Inheritance - the mechanism that allows one class to acquire all the properties from another class by inheriting the class. 
// Inheritance. For example:
public class Car extends Vehicle { 
    //...
}

When we extend a class, we form an IS-A relationship. The Car IS-A Vehicle. So, it has all the characteristics of a Vehicle. 
method is speed or method contains primitve types and there method. 
behavior is setSpeed.

// Example of inheritance also.
public class Vehicle {
    private int wheels;
    private String model;
    public void start() {
        // the process of starting the vehicle
    }
    
    public void stop() {
        // process to stop the vehicle
    }
    
    public void honk() { 
        // produces a default honk 
    }

}

// Example of Inhertance:
public class ArmoredCar extends Car {
    private boolean bulletProofWindows;
    
    public void remoteStartCar() {
        // this vehicle can be started by using a remote control
    }
}

Here, the ArmouredCar extends Car, and Car extends Vehicle. So, ArmouredCar inherits properties from both Car and Vehicle. This is known as method overriding.



Polymorphism - the ability of an OOP language to process data depending on their types of inputs differently. 
// Polymorphism. For instance: 
public class TextFile extends GenericFile {
    //...
 
    public String read() {
        return this.getContent()
          .toString();
    }
 
    public String read(int limit) {
        return this.getContent()
          .toString()
          .substring(0, limit);
    }
 
    public String read(int start, int stop) {
        return this.getContent()
          .toString()
          .substring(start, stop);
    }
}

This type of polymorphism is static or compile-time polymorphism and is also called method overloading.
// Polymorphism. For example,
public class GenericFile {
    private String name;
 
    //...
 
    public String getFileInfo() {
        return "Generic File Impl";
    }
}

There is also runtime or dynamic polymorphism, where the child class overrides the parent’s method:
// Polymophism. For example,
public class ImageFile extends GenericFile {
    private int height;
    private int width;
 
    //... getters and setters
     
    public String getFileInfo() {
        return "Image File Impl";
    }
}

A child class can extend the GenericFile class and override the getFileInfo() method:



Conclusion
OOP contains, abstraction, objects, inheritance, classes, polymorphism, encapsulation. 
- Monitoring
- OVM

