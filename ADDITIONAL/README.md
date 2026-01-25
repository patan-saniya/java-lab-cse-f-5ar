# Additional-1
# Title:To write a java program to insert substring in mainstring.
# Source code:
# Substringinsert.java:
``` java
import java.util.Scanner;

class SubstringInsert {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String mainString;
        String subString;
        int position;

        System.out.print("Enter the main string: ");
        mainString = sc.nextLine();

        System.out.print("Enter the substring: ");
        subString = sc.nextLine();

        System.out.print("Enter the position to insert: ");
        position = sc.nextInt();

        int length = mainString.length();
        String resultString;

        if (position >= 0 && position <= length) {
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            resultString = firstPart + subString + secondPart;

            System.out.println("Resultant String = " + resultString);
        } else {
            System.out.println("Substring cannot be inserted.");
            System.out.println("Condition: 0 <= position <= " + length);
        }

        sc.close();
    }
}
```
# Output:

# Additional-2
# Title:To write a program to find the sum of the first 'n' fibonacci number.
# Source code:
# Fibonacci.java
``` java
import java.util.Scanner;

class Fibonacci {
    int sum;
    int n;
    int firstNumber;
    int secondNumber;
    int thirdNumber;

    Fibonacci(int number) {
        n = number;
        firstNumber = 0;
        secondNumber = 1;
        thirdNumber = 0;
        sum = 0;
    }

    void generate() {
        if (n > 0) {
            System.out.print("Fibonacci series: ");
        }

        while (n > 0) {
            if (n == 1) {
                System.out.println(firstNumber + ".");
                sum = sum + firstNumber;
            } else {
                System.out.print(firstNumber + ", ");
                sum = sum + firstNumber;
            }

            thirdNumber = firstNumber + secondNumber;
            firstNumber = secondNumber;
            secondNumber = thirdNumber;
            n--;
        }

        System.out.println("Sum of Fibonacci series = " + sum);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the value of n: ");
        int number = sc.nextInt();

        Fibonacci f = new Fibonacci(number);
        f.generate();
    }
}
```
# Output:


# Additional-3
# Title:To write a java program to find the palindrome or not.
#  Source code:
# Palindrome.java:
``` java
import java.util.Scanner;

class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the string: ");
        String str = sc.nextLine();

        int start = 0;
        int end = str.length() - 1;
        boolean flag = true;

        while (start < end) {
            if (str.charAt(start) != str.charAt(end)) {
                System.out.println("String is not a palindrome");
                flag = false;
                break;
            }
            start++;
            end--;
        }

        if (flag) {
            System.out.println("String is a palindrome");
        }

        sc.close();
    }
}
```
# Output:

# Additional-4
# Title:TO write a java program to find the perfect or not.
# Source code:
# Perfect.java:
``` java
import java.util.Scanner;

class Perfect {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the perfect number: ");
        int num = sc.nextInt();

        int sum = 0;

        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }

        if (sum == num && num != 0) {
            System.out.println(num + " is a Perfect Number");
        } else {
            System.out.println(num + " is not a Perfect Number");
        }

        sc.close();
    }
}
```
# Output:
