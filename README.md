Chapter 2

Key Concepts
Objects: Real-world entities with properties (attributes) and behaviors (methods).
Classes: Blueprints for creating objects.
Attributes: Data stored within an object.
Methods: Actions that an object can perform.
Instance Variables: Variables declared within a class that belong to individual objects.
Methods: Functions defined within a class that can be called on objects.

Creating and Using Objects
Declaring a Class: Use the class keyword followed by the class name.
Creating an Object: Use the new keyword with the class name.
Accessing Attributes: Use the dot notation (.) to access an object's attributes.
Calling Methods: Use the dot notation (.) to call an object's methods.

Example:
Java
class Dog {
    String name;
    int age;

    void bark() {
        System.out.println("Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog fido = new Dog();
        fido.name = "Fido";
        fido.age = 3;
        fido.bark();
    }
}

Encapsulation: Hiding the internal implementation of an object from the outside world.
Inheritance: Creating new classes based on existing classes.
Polymorphism: The ability of objects of different types to respond to the same message in different ways.

Chapter 3

Key Concepts
Methods: Reusable blocks of code that perform specific tasks.
Parameters: Values passed to a method when it's called.
Return Values: Values that a method can send back to the caller.
Method Overloading: Creating multiple methods with the same name but different parameters.
Variable Scope: The region of a program where a variable is visible.

Creating and Using Methods
Declaring a Method: Use the public, private, static, and return type keywords followed by the method name and parameters.
Calling a Method: Use the dot notation (.) to call a method on an object.
Passing Arguments: Provide values for the parameters when calling a method.
Returning Values: Use the return keyword to send a value back from a method.


Example:
Java
class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public void printMessage(String message) {
        System.out.println(message);
    }
}

public class Main {
    public static void main(String[] args)   
 {
        Calculator calc = new Calculator();
        int result = calc.add(2, 3);
        System.out.println("Result: " + result);

        calc.printMessage("Hello,   
 world!");
    }
}

Method Overloading: Methods with the same name but different parameters can be overloaded. The compiler determines which method to call based on the number and types of arguments provided.
Variable Scope: Variables declared within a method have local scope and are only visible within that method. Variables declared outside of methods have class scope and are visible throughout the class.

Chapter 4

Key Concepts
Inheritance: Creating new classes (subclasses) based on existing classes (superclasses).
Superclass: The class that other classes inherit from.
Subclass: A class that inherits from another class.
Overriding: Providing a different implementation of a method in a subclass.
Polymorphism: The ability of objects of different types to be treated as if they were of the same type.

Creating Subclasses
Use the extends keyword to declare a subclass.
Subclasses inherit all public and protected members from their superclass.
Subclasses can override methods defined in the superclass.
Overriding Methods
Use the @Override annotation (optional) to indicate that a method is overriding a superclass method.
The overridden method must have the same signature (name, return type, and parameters) as the superclass method.

Using the super Keyword
Use the super keyword to access members of the superclass from within a subclass.
Use super() to call the superclass's constructor.

Polymorphism
Objects of different types can be treated as if they were of the same type if they are related through inheritance.
This allows for more flexible and reusable code.

Example:
Java
class Animal {
    void makeSound() {
        System.out.println("Generic sound");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof!");
    }
}

class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Meow!");
    }
}

public class   
 Main {
    public static void main(String[] args) {
        Animal[] animals = {new Dog(), new Cat()};
        for (Animal animal : animals) {
            animal.makeSound();   

        }
    }
}
