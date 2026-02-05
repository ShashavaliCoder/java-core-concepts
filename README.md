Java Core Concepts – Theory & Examples

This repository contains core Java concepts explained with clear theory and practical examples.
The goal is interview readiness + strong fundamentals, not just running code.

📁 Project Structure
Java-Core-Concepts/
├── Constructors/
├── OOPS/
├── ExceptionHandling/
├── MultiThreading/
├── Collections/
└── README.md


Each folder:

Represents one Java concept

Contains theory-based examples

Uses proper package naming

1️⃣ Constructors
📌 Theory

A constructor is a special method used to initialize objects.

Same name as class

No return type

Called automatically when object is created

Types

Default Constructor

Zero-Parameter Constructor

Parameterized Constructor

Constructor Overloading

Example
class Student {
    int id;
    String name;

    Student() {              // Zero-parameter constructor
        id = 0;
        name = "Unknown";
    }

    Student(int i, String n) { // Parameterized constructor
        id = i;
        name = n;
    }
}

2️⃣ OOPS Concepts
📌 Core Principles

Encapsulation

Inheritance

Polymorphism

Abstraction

🔹 Encapsulation

Wrapping data + methods into a single unit.

class Account {
    private double balance;

    public void setBalance(double b) {
        balance = b;
    }

    public double getBalance() {
        return balance;
    }
}

🔹 Inheritance

One class acquires properties of another.

class Animal {
    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking");
    }
}

🔹 Polymorphism

Same method name, different behavior.

class MathUtil {
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}

🔹 Abstraction

Hiding implementation details.

abstract class Vehicle {
    abstract void start();
}

class Bike extends Vehicle {
    void start() {
        System.out.println("Bike starts");
    }
}

3️⃣ Exception Handling
📌 Theory

Exception handling prevents program termination during runtime errors.

Keywords

try

catch

finally

throw

throws

🔹 Basic Example
try {
    int a = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero");
}

🔹 Ducking Exception (throws)
void readFile() throws IOException {
    FileReader fr = new FileReader("data.txt");
}

🔹 Re-throwing Exception
try {
    int x = 10 / 0;
} catch (Exception e) {
    throw e;
}

4️⃣ Multithreading
📌 Theory

Multithreading allows multiple threads to run concurrently, improving performance.

Ways to create threads

Extending Thread

Implementing Runnable

🔹 Using Thread Class
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread running");
    }
}

🔹 Using Runnable
class MyTask implements Runnable {
    public void run() {
        System.out.println("Runnable thread");
    }
}

🔹 Thread Lifecycle

New

Runnable

Running

Waiting

Terminated

5️⃣ Collections Framework
📌 Theory

Collections framework is used to store, manipulate, and retrieve data efficiently.

Core Interfaces

List

Set

Queue

Map

🔹 List (ArrayList)
List<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");

🔹 Set (HashSet)
Set<Integer> set = new HashSet<>();
set.add(10);
set.add(10); // duplicates not allowed

🔹 Map (HashMap)
Map<Integer, String> map = new HashMap<>();
map.put(1, "One");
map.put(2, "Two");

🔹 Iterator Example
Iterator<String> it = list.iterator();
while (it.hasNext()) {
    System.out.println(it.next());
}
