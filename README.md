[program-1 wap for arithmatic logics](#assi-1)

[program-2 wap for hello world](#assi-2)   

[program-3 wap for the addition of two distances where each distance is given in meter, c-m](#assi-3)

[program-4 wap for the addition of two times where each time is given in hours, minutes](#assi-4)

[program-5 wap for the addition of two times where each time is given in hours, minutes and seconds](#assi-5)

[program-6 wap for the addition of two distance where each distance is given in meter, centi-meter and millimeter](#assi-6)

[program-7 wap using object and classes to do the reverse of 1d array](#assi-7)

[program-8 write a class of implementationoperation of matrix(3*3): 1.transpose 2.sum 3.multiply 4.sum of rows 5.sum of columns 6.sum of diagonal](#assi-8)

[program-9 collect the code of c language for any 5 operation, convert the logic to java in object oriented fashion](#assi-9)




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

public class DistanceAddition { //declares the main class
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); // creates a scanner object named sc

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
public class MatrixOperations {

    int[][] A = {
        {1,2,3},
        {4,5,6},
        {7,8,9}
    };

    int[][] B = {
        {9,8,7},
        {6,5,4},
        {3,2,1}
    };

    void display(int[][] M){
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(M[i][j]+" ");
            }
            System.out.println();
        }
    }

    void transpose(){
        int[][] T = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                T[j][i] = A[i][j];
            }
        }

        System.out.println("Transpose of Matrix A:");
        display(T);
    }

    void sum(){
        int[][] S = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                S[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Sum of A and B:");
        display(S);
    }

    void multiply(){
        int[][] M = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                for(int k=0;k<3;k++){
                    M[i][j] += A[i][k]*B[k][j];
                }
            }
        }

        System.out.println("Multiplication of A and B:");
        display(M);
    }

    void rowSum(){
        for(int i=0;i<3;i++){
            int sum=0;
            for(int j=0;j<3;j++){
                sum += A[i][j];
            }
            System.out.println("Row "+(i+1)+" Sum = "+sum);
        }
    }

    void columnSum(){
        for(int j=0;j<3;j++){
            int sum=0;
            for(int i=0;i<3;i++){
                sum += A[i][j];
            }
            System.out.println("Column "+(j+1)+" Sum = "+sum);
        }
    }

    void diagonalSum(){
        int p=0,s=0;

        for(int i=0;i<3;i++){
            p += A[i][i];
            s += A[i][2-i];
        }

        System.out.println("Primary Diagonal Sum = "+p);
        System.out.println("Secondary Diagonal Sum = "+s);
    }

    public static void main(String[] args){

        MatrixOperations obj = new MatrixOperations();

        System.out.println("Matrix A:");
        obj.display(obj.A);

        System.out.println("Matrix B:");
        obj.display(obj.B);

        obj.transpose();
        obj.sum();
        obj.multiply();
        obj.rowSum();
        obj.columnSum();
        obj.diagonalSum();
    }
}

```
<img width="320" height="416" alt="image" src="https://github.com/user-attachments/assets/22b8ca3b-ba26-4dc7-a504-80db0b26191b" />

## assi-9

```
public class NumberOperations {

    int num = 5;     // for factorial & fibonacci
    int pal = 121;   // for palindrome
    int arm = 153;   // for armstrong

    // 1. Factorial
    void factorial() {
        int fact = 1;

        for (int i = 1; i <= num; i++) {
            fact *= i;
        }

        System.out.println("Factorial of " + num + " = " + fact);
    }

    // 2. Fibonacci Series
    void fibonacci() {
        int a = 0, b = 1;

        System.out.println("Fibonacci series:");

        for (int i = 1; i <= num; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }

        System.out.println();
    }

    // 3. Palindrome Number
    void palindrome() {
        int temp = pal;
        int rev = 0;

        while (temp > 0) {
            int digit = temp % 10;
            rev = rev * 10 + digit;
            temp /= 10;
        }

        if (pal == rev)
            System.out.println(pal + " is Palindrome");
        else
            System.out.println(pal + " is Not Palindrome");
    }

    // 4. Armstrong Number
    void armstrong() {
        int temp = arm;
        int sum = 0;

        while (temp > 0) {
            int digit = temp % 10;
            sum += digit * digit * digit;
            temp /= 10;
        }

        if (sum == arm)
            System.out.println(arm + " is Armstrong");
        else
            System.out.println(arm + " is Not Armstrong");
    }

    // 5. Pattern
    void pattern() {
        System.out.println("Pattern:");

        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    // Main method
    public static void main(String[] args) {

        NumberOperations obj = new NumberOperations();

        obj.factorial();
        obj.fibonacci();
        obj.palindrome();
        obj.armstrong();
        obj.pattern();
    }
}

```

<img width="302" height="175" alt="image" src="https://github.com/user-attachments/assets/fe7be21e-8d38-427a-8157-a189807715cf" />





        


