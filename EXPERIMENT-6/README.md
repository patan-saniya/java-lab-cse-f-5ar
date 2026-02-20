# Exp-6a
# Title : To describe  exception handling mechanism
# Source code:
``` java
// ArrayInput.java
import java.util.Scanner;

public class ArrayInput {

    public int[] readArray() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        return arr;
    }
}
```
``` java
// ArrayAccess.java
import java.util.Scanner;

public class ArrayAccess {

    public void accessElement(int[] arr) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the index to access: ");
        int index = sc.nextInt();

        try {
            System.out.println("Element at index " + index + " is: " + arr[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println(
                "Invalid index! Please enter an index between 0 and " + (arr.length - 1)
            );
        }
    }
}
```
``` java
// ExceptionHandlingDemo.java

public class ExceptionHandlingDemo {

    public static void main(String[] args) {

        ArrayInput input = new ArrayInput();
        int[] array = input.readArray();

        ArrayAccess access = new ArrayAccess();
        access.accessElement(array);
    }
}
```
