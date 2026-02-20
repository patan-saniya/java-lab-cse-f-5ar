# Exp-4a
# Title:To write a java program to implement single inharitance.
# Source code:
# Person:
``` java
// Base class
class Person {
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display person details
    void displayPersonDetails() {
        System.out.println("Name : " + name);
        System.out.println("Age  : " + age);
    }
}
```
# Employee:
``` java
// Derived class
class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String insuranceNumber;

    // Constructor
    Employee(String name, int age, double annualSalary, int yearOfJoining, String insuranceNumber) {
        super(name, age); // call parent class constructor
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.insuranceNumber = insuranceNumber;
    }

    // Method to display employee details
    void displayEmployeeDetails() {
        displayPersonDetails(); // inherited method
        System.out.println("Annual Salary : " + annualSalary);
        System.out.println("Year of Joining : " + yearOfJoining);
        System.out.println("Insurance Number : " + insuranceNumber);
    }
}
```
# TestEmployee:
``` java
public class TestEmployee {
    public static void main(String[] args) {
        Employee emp = new Employee(
                "Karthik",
                22,
                450000.50,
                2024,
                "INS12345"
        );

        emp.displayEmployeeDetails();
    }
}
```
# Output:
# Exp-4b
# Title : To implement multilevel inheritance
# Sorce code:
# Bicycle:
``` java
// Bicycle.java
public class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals.");
        System.out.println("Pedal Type : " + pedalType);
    }
}
```
 # Motorbike.java
``` java
// Motorbike.java
public class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine.");
        System.out.println("Engine Capacity : " + engineCapacity + " cc");
    }
}
```
 # ElectricBike
 ``` java
// ElectricBike.java
public class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor and battery.");
        System.out.println("Battery Capacity : " + batteryCapacity + " Wh");
    }
}
```
# TestVehicle
``` java
// TestVehicle.java
public class TestVehicle {
    public static void main(String[] args) {

        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 150;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();      // from Bicycle
        eBike.showMotorbikeInfo();    // from Motorbike
        eBike.showElectricBikeInfo(); // from ElectricBike
    }
}
```
# Output:
# Exp-4c
# Title : To construct abstract class
# Source code:
# Figure:
``` java
// Figure.java
abstract class Figure {
    double dim1;
    double dim2;

    // Constructor
    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
    }

    // Abstract method
    abstract double area();
}
```
# Rectangle
``` java
// Rectangle.java
class Rectangle extends Figure {

    // Constructor
    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    // Implementing abstract method
    double area() {
        return dim1 * dim2;
    }
}
```
# Triangle
``` java
// Triangle.java
class Triangle extends Figure {

    // Constructor
    Triangle(double base, double height) {
        super(base, height);
    }

    // Implementing abstract method
    double area() {
        return 0.5 * dim1 * dim2;
    }
}
```
# TestFigure
``` java
// TestFigure.java
public class TestFigure {
    public static void main(String[] args) {

        Figure f1 = new Rectangle(10, 5);
        System.out.println("Area of Rectangle = " + f1.area());

        Figure f2 = new Triangle(8, 6);
        System.out.println("Area of Triangle = " + f2.area());
    }
}
```
# Output:
