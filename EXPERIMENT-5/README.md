# Exp-5a
# Title : To implement inheritance
# Source code:
# sortable
``` java
// Interface
interface Sortable {
    void sort(int[] arr);
}
```
# Bubblesort:
``` java
// BubbleSort class implementing Sortable
class BubbleSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {

                if (arr[j] > arr[j + 1]) {
                    // swap
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}
```
# Selectionsort:
``` java
// SelectionSort class implementing Sortable
class SelectionSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {

            int minIndex = i;

            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }

            // swap
            int temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
        }
    }
}
```
# Testsort:
``` java
// Main class
public class TestSort {

    public static void main(String[] args) {

        int[] arr1 = {5, 2, 9, 1, 3};

        Sortable ref;

        ref = new BubbleSort();
        ref.sort(arr1);

        System.out.println("Array sorted using BubbleSort:");
        display(arr1);

        int[] arr2 = {8, 4, 7, 6, 2};

        ref = new SelectionSort();
        ref.sort(arr2);

        System.out.println("Array sorted using SelectionSort:");
        display(arr2);
    }

    static void display(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}
```
# Output:

# Exp-5b
# Title : To implement runtime polymorphism
# Source code:
# Vehicle:
``` java
// Base class
class Vehicle {

    void run() {
        System.out.println("Vehicle is running");
    }
}
```
# car:
``` java
// Subclass Car
class Car extends Vehicle {

    @Override
    void run() {
        System.out.println("Car is running on four wheels");
    }
}
```
# Bike:
``` java
// Subclass Bike
class Bike extends Vehicle {

    @Override
    void run() {
        System.out.println("Bike is running on two wheels");
    }
}
```
# TestVehicle:
``` java
// Main class
public class TestVehicle {

    public static void main(String[] args) {

        Vehicle v;   // base class reference

        v = new Car();
        v.run();     // calls Car's run()

        v = new Bike();
        v.run();     // calls Bike's run()

        v = new Vehicle();
        v.run();     // calls Vehicle's run()
    }
}
```
# Ouput:
# Exp-5c
# Title : TO use stringbuffer to delete,remove character
# Source code:
# Deletechar:
``` java
public class StringBufferDeleteDemo {

    public static void main(String[] args) {

        // Create StringBuffer object
        StringBuffer sb = new StringBuffer("Java Programming");

        // Display original string
        System.out.println("Original String: " + sb);

        // Delete a single character at index 4
        sb.deleteCharAt(4);
        System.out.println("After deleting character at index 4: " + sb);

        // Delete a range of characters from index 0 to 4
        sb.delete(0, 4);
        System.out.println("After deleting characters from index 0 to 4: " + sb);
    }
}
```
