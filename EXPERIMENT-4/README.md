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
```
# Output:
# Exp-4c
# Title : To construct abstract class
# Source code:
# Figure:
