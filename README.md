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


