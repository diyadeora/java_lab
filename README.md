[program-1 wap for arithmatic logics](#assi-1)

[program-2 wap for hello world](#assi-2)   

[program-3 wap for the addition of two distances where each distance is given in meter, c-m](#assi-3)

[program-4 wap for the addition of two times where each time is given in hours, minutes](#assi-4)

[program-5 wap for the addition of two times where each time is given in hours, minutes and seconds](#assi-5)

[program-6 wap for the addition of two distance where each distance is given in meter, centi-meter and millimeter](#assi-6)

[program-7 wap using object and classes to do the reverse of 1d array](#assi-7)

[program-8 wap for transpose of matrix 3*3](#assi-8)

[program-9 wap for sum of matrix](#assi-9)

[program-10 wap for multiply of matrix](#assi-10)

[program-11 wap for sum of rows of matrix](#assi-11)

[program-12 wap for sum of columns of matrix](#assi-12)

[program-13 wap for sum of diagonals of matrix](#assi-13)

[program-14 wap for factorial of numbers](#assi-14)

[program-15 wap for fabannoic series](#assi-15)

[program-16 wap for palendrome numbers](#assi-16)

[program-17 wap for armstrong numbers](#assi-17)

[program-18 wap for making patterns](#assi-18)

[program-19 wap for ](#assi-19)

[program-20 wap for ](#assi-20)

[program-21 wap for](#assi-21)

[program-22 wap for](#assi-22)

[program-23 wap for](#assi-23)

[program-24 wap for](#assi-24)

## assi-1
```
public class Cla{
static int add(int a,int b){
return a+b;
}
static int sub(int a,int b){
return a-b;
}
static int mul(int a,int b){
return a*b;
}
static int div(int a,int b){
return a/b;
}
public static void main(String[]args){
int n1=Integer.parseInt(args[0]);
int n2=Integer.parseInt(args[1]);
System.out.println(add(n1,n2));
System.out.println(sub(n1,n2));
System.out.println(mul(n1,n2));
System.out.println(div(n1,n2));
}
}
```
<img width="867" height="79" alt="image" src="https://github.com/user-attachments/assets/4813d2f8-ea7f-460d-b95f-27d19bbc83e0" />

## assi-2
```
class Hey{
    public static void main(String args[]){
        System.out.println("hello");
    }
}

```
<img width="1613" height="99" alt="image" src="https://github.com/user-attachments/assets/8566a3e4-d945-4220-8454-350b8460a533" />

## assi-3
```
import java.util.Scanner;

class Distance {
    int meters;
    int centimeters;
}

public class DistanceAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance result = new Distance();

        System.out.println("Enter first distance (meters centimeters):");
        d1.meters = sc.nextInt();
        d1.centimeters = sc.nextInt();

        System.out.println("Enter second distance (meters centimeters):");
        d2.meters = sc.nextInt();
        d2.centimeters = sc.nextInt();

        // Add centimeters
        result.centimeters = d1.centimeters + d2.centimeters;
        result.meters = d1.meters + d2.meters;

        // Convert extra centimeters to meters
        if (result.centimeters >= 100) {
            result.meters += result.centimeters / 100;
            result.centimeters = result.centimeters % 100;
        }

        System.out.println("Sum of distances = " + result.meters + 
                " meters " + result.centimeters + " centimeters");

        sc.close();
    }
}
```
<img width="673" height="374" alt="image" src="https://github.com/user-attachments/assets/b129ad7c-3423-4fd7-8218-ce01ddac8d42" />

## assi-4
```
import java.util.Scanner;

class Time {
    int hours;
    int minutes;
}

public class TimeAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Time t1 = new Time();
        Time t2 = new Time();
        Time result = new Time();

        System.out.println("Enter first time (hours minutes):");
        t1.hours = sc.nextInt();
        t1.minutes = sc.nextInt();

        System.out.println("Enter second time (hours minutes):");
        t2.hours = sc.nextInt();
        t2.minutes = sc.nextInt();

        // Add minutes
        result.minutes = t1.minutes + t2.minutes;
        result.hours = t1.hours + t2.hours;

        // Convert extra minutes to hours
        if (result.minutes >= 60) {
            result.hours += result.minutes / 60;
            result.minutes = result.minutes % 60;
        }

        System.out.println("Sum of time = " + result.hours + 
                " hours " + result.minutes + " minutes");

        sc.close();
    }
}

```
<img width="626" height="305" alt="image" src="https://github.com/user-attachments/assets/0f2e6446-8e89-477e-9b6f-0c98f635cfaa" />

## assi-5
```

import java.util.Scanner;

class Time {
    int hours;
    int minutes;
    int seconds;
}

public class TimeAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Time t1 = new Time();
        Time t2 = new Time();

        System.out.println("Enter first time (hours minutes seconds):");
        t1.hours = sc.nextInt();
        t1.minutes = sc.nextInt();
        t1.seconds = sc.nextInt();

        System.out.println("Enter second time (hours minutes seconds):");
        t2.hours = sc.nextInt();
        t2.minutes = sc.nextInt();
        t2.seconds = sc.nextInt();

        // Convert total time into seconds
        int totalSeconds = (t1.hours * 3600 + t1.minutes * 60 + t1.seconds)
                         + (t2.hours * 3600 + t2.minutes * 60 + t2.seconds);

        // Convert back to hours, minutes, and seconds
        int resultHours = totalSeconds / 3600;
        totalSeconds = totalSeconds % 3600;
        int resultMinutes = totalSeconds / 60;
        int resultSeconds = totalSeconds % 60;

        System.out.println("Sum of time = " + resultHours + " hours "
                + resultMinutes + " minutes " + resultSeconds + " seconds");

        sc.close();
    }
}

```
<img width="608" height="383" alt="image" src="https://github.com/user-attachments/assets/64f73315-7f1d-47cb-8caa-93579fd640fa" />

## assi-6

```

import java.util.Scanner;

class Distance {
    int meters;
    int centimeters;
    int millimeters;
}

public class DistanceAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter first distance (meters centimeters millimeters):");
        d1.meters = sc.nextInt();
        d1.centimeters = sc.nextInt();
        d1.millimeters = sc.nextInt();

        System.out.println("Enter second distance (meters centimeters millimeters):");
        d2.meters = sc.nextInt();
        d2.centimeters = sc.nextInt();
        d2.millimeters = sc.nextInt();

        // Convert both distances to millimeters
        int totalMillimeters = (d1.meters * 1000 + d1.centimeters * 10 + d1.millimeters)
                            + (d2.meters * 1000 + d2.centimeters * 10 + d2.millimeters);

        // Convert back to meters, centimeters, and millimeters
        int resultMeters = totalMillimeters / 1000;
        totalMillimeters = totalMillimeters % 1000;
        int resultCentimeters = totalMillimeters / 10;
        int resultMillimeters = totalMillimeters % 10;

        System.out.println("Sum of distances = " + resultMeters + " meters "
                + resultCentimeters + " centimeters " + resultMillimeters + " millimeters");

        sc.close();
    }
}
```

<img width="793" height="345" alt="image" src="https://github.com/user-attachments/assets/2bbce30e-5fa5-4d40-baf2-3c7bc8bb5a3d" />

## assi-7

```

import java.util.Scanner;

public class ReverseArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int arr[] = new int[n];

        System.out.println("Enter elements:");
        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Reversing array
        System.out.println("Reversed array:");
        for(int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }

        sc.close();
    }
}

```
<img width="665" height="376" alt="image" src="https://github.com/user-attachments/assets/0b326ff2-5fcb-4466-a303-84a83a1514c6" />

## assi-8

```
class TransposeMatrix {
    int a[][] = new int[3][3];
    int t[][] = new int[3][3];

    void input() {
        int k = 1;
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                a[i][j] = k;
                k++;
            }
        }
    }

    void transpose() {
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                t[i][j] = a[j][i];
            }
        }
    }

    void display() {
        System.out.println("Original Matrix:");
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println("Transpose Matrix:");
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.print(t[i][j] + " ");
            }
            System.out.println();
        }
    }

    public static void main(String args[]) {
        TransposeMatrix obj = new TransposeMatrix();
        obj.input();
        obj.transpose();
        obj.display();
    }
}

```

<img width="738" height="365" alt="image" src="https://github.com/user-attachments/assets/30f6b5e9-c301-4f46-a3fa-b8cffed9c018" />

## assi-9

```
class SumMatrix {
    int a[][] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
    int sum = 0;

    void calculateSum() {
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                sum = sum + a[i][j];
            }
        }
    }

    void display() {
        System.out.println("Matrix:");
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println("Sum of all elements = " + sum);
    }

    public static void main(String args[]) {
        SumMatrix obj = new SumMatrix();
        obj.calculateSum();
        obj.display();
    }
}

```

<img width="618" height="268" alt="image" src="https://github.com/user-attachments/assets/7b6b88b6-16ec-45f2-81f0-641ca9de00bc" />

## assi-10

```

class MatrixMultiplication {
    int a[][] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int b[][] = {
        {1, 2, 1},
        {2, 1, 2},
        {1, 2, 1}
    };

    int c[][] = new int[3][3];

    void multiply() {
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                for(int k = 0; k < 3; k++) {
                    c[i][j] = c[i][j] + a[i][k] * b[k][j];
                }
            }
        }
    }

    void display() {
        System.out.println("Result Matrix:");
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                System.out.print(c[i][j] + " ");
            }
            System.out.println();
        }
    }

    public static void main(String args[]) {
        MatrixMultiplication obj = new MatrixMultiplication();
        obj.multiply();
        obj.display();
    }
}

```

<img width="385" height="149" alt="image" src="https://github.com/user-attachments/assets/e6d2221c-004c-43d2-91e9-b31656f3de4e" />

## assi-11

```
class RowSum {
    int a[][] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    void sumRows() {
        for(int i = 0; i < 3; i++) {
            int sum = 0;
            for(int j = 0; j < 3; j++) {
                sum = sum + a[i][j];
            }
            System.out.println("Sum of row " + (i+1) + " = " + sum);
        }
    }

    public static void main(String args[]) {
        RowSum obj = new RowSum();
        obj.sumRows();
    }
}

```
<img width="281" height="109" alt="image" src="https://github.com/user-attachments/assets/dd1f5c56-2498-47c3-a1d7-1c37c71c7ef2" />

## assi-12

```
class ColumnSum {
    int a[][] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    void sumColumns() {
        for(int j = 0; j < 3; j++) {
            int sum = 0;
            for(int i = 0; i < 3; i++) {
                sum = sum + a[i][j];
            }
            System.out.println("Sum of column " + (j+1) + " = " + sum);
        }
    }

    public static void main(String args[]) {
        ColumnSum obj = new ColumnSum();
        obj.sumColumns();
    }
}

```
<img width="290" height="107" alt="image" src="https://github.com/user-attachments/assets/40c0603d-7551-449b-80ec-a3a5d0f816c4" />

## assi-13

```

class DiagonalSum {
    int a[][] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    void sumDiagonals() {
        int primary = 0, secondary = 0;

        for(int i = 0; i < 3; i++) {
            primary = primary + a[i][i];
            secondary = secondary + a[i][2 - i];
        }

        System.out.println("Sum of Primary Diagonal = " + primary);
        System.out.println("Sum of Secondary Diagonal = " + secondary);
    }

    public static void main(String args[]) {
        DiagonalSum obj = new DiagonalSum();
        obj.sumDiagonals();
    }
}

```

<img width="305" height="80" alt="image" src="https://github.com/user-attachments/assets/2cc3d626-40df-4b2c-a55b-05ce49cbfd63" />

## assi-14

```
class Factorial {
    int fact = 1;

    void calculate(int n) {
        for(int i = 1; i <= n; i++) {
            fact = fact * i;
        }
        System.out.println("Factorial = " + fact);
    }

    public static void main(String args[]) {
        Factorial obj = new Factorial();
        obj.calculate(5);
    }
     }

```

<img width="309" height="67" alt="image" src="https://github.com/user-attachments/assets/d793add4-ea0b-4354-a1e3-b7ad7c800b87" />

## assi-15

```
class Fibonacci {
    void series(int n) {
        int a = 0, b = 1, c;
        System.out.print(a + " " + b);

        for (int i = 2; i < n; i++) {
            c = a + b;
            System.out.print(" " + c);
            a = b;
            b = c;
        }
    }

    public static void main(String args[]) {
        Fibonacci obj = new Fibonacci();
        obj.series(10);
    }
}

```

<img width="299" height="65" alt="image" src="https://github.com/user-attachments/assets/0478f4a0-6641-4351-a6a8-34684c4f419c" />

## assi-16

```
class Palindrome {
    void check(int n) {
        int temp = n, rev = 0, rem;

        while (temp != 0) {
            rem = temp % 10;
            rev = rev * 10 + rem;
            temp = temp / 10;
        }

        if (rev == n)
            System.out.println("Palindrome Number");
        else
            System.out.println("Not a Palindrome Number");
    }

    public static void main(String args[]) {
        Palindrome obj = new Palindrome();
        obj.check(121);
    }
}

```

<img width="311" height="70" alt="image" src="https://github.com/user-attachments/assets/f14fa585-7b21-4ade-be50-d104f36c18e2" />

## assi-17

```
class Armstrong {
    void check(int n) {
        int temp = n, sum = 0, rem;

        while (temp != 0) {
            rem = temp % 10;
            sum = sum + (rem * rem * rem);
            temp = temp / 10;
        }

        if (sum == n)
            System.out.println("Armstrong Number");
        else
            System.out.println("Not Armstrong Number");
    }

    public static void main(String args[]) {
        Armstrong obj = new Armstrong();
        obj.check(153);
    }
}

```

<img width="306" height="77" alt="image" src="https://github.com/user-attachments/assets/eb86467d-b2ee-44ea-9e9e-41c32af916c3" />















