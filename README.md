[program-1 wap for arithmatic logics](#assi-1)

[program-2 wap for hello world](#assi-2)   

[program-3 wap for the addition of two distances where each distance is given in meter, c-m](#assi-3)

[program-4 wap for the addition of two times where each time is given in hours, minutes](#assi-4)

[program-5 wap for the addition of two times where each time is given in hours, minutes and seconds](#assi-5)

[program-6 wap for the addition of two distance where each distance is given in meter, centi-meter and millimeter](#assi-6)

[program-7 wap using object and classes to do the reverse of 1d array](#assi-7)

[program-8 write a class of implementationoperation of matrix(3*3): 1.transpose 2.sum 3.multiply 4.sum of rows 5.sum of columns 6.sum of diagonal](#assi-8)

[program-9 collect the code of c language for any 5 operation, convert the logic to java in object oriented fashion](#assi-9)

[program-10 demonstrate all 3 types of inheritance 1.single 2.multilevel 3.hierarchial](#assi-10)

[program-11 write a program using three classes to print 1-100,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface](#assi-11)

[program-12 using the concept of multithreading the output of all three threads must be synchronised (use join method)](#assi-12)

[program-13 addition of two numbers using swing](#assi-13)

[program-14 make a registration form with 10 elements and send the data into database(using jdbc connectivity)](#assi-14)

[program-15 make one calculator in swing](#assi-15)

[program-16 matrix addition using swing class](#assi-16)

[program-17 create one jframe apply 10 buttons on that after clicking on each button a new button structure is created(circle,oval rectangle,etc...)](#assi-17)

[program-18 just using mouse event craete a frame like paint brush with selection of colour and width ](#assi-18)

[program-19 create a package of any 5 classes of your choice and import it](#assi-19)

[program-20 create one package and sub package import and test it](#assi-20)

[program-21 create one small array of size 5 apply array out of bounds exception using try catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception](#assi-21)

[program-22 to test the range of age of one student.write a program using user defined exception.](#assi-22)

[program-23 file handling programs](#assi-23)

[program-24 inheritance program using interface and abstract classes](#assi-24)

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

## assi-10

```
// Base class
public class A {

    void showA() {
        System.out.println("Class A (Parent)");
    }

    public static void main(String[] args) {

        // Single Inheritance
        System.out.println("Single Inheritance:");
        B obj1 = new B();
        obj1.showA();
        obj1.showB();

        // Multilevel Inheritance
        System.out.println("\nMultilevel Inheritance:");
        C obj2 = new C();
        obj2.showA();
        obj2.showB();
        obj2.showC();

        // Hierarchical Inheritance
        System.out.println("\nHierarchical Inheritance:");
        D obj3 = new D();
        E obj4 = new E();

        obj3.showA();
        obj3.showD();

        obj4.showA();
        obj4.showE();
    }
}

// Single Inheritance
class B extends A {
    void showB() {
        System.out.println("Class B (Child of A)");
    }
}

// Multilevel Inheritance
class C extends B {
    void showC() {
        System.out.println("Class C (Child of B)");
    }
}

// Hierarchical Inheritance
class D extends A {
    void showD() {
        System.out.println("Class D (Another Child of A)");
    }
}

class E extends A {
    void showE() {
        System.out.println("Class E (Another Child of A)");
    }
}
```
<img width="260" height="230" alt="image" src="https://github.com/user-attachments/assets/aad082ae-b2d5-4d14-a01c-5129ad16f25a" />

## assi-11

'''
class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A (Normal): " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B (Normal): " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C (Normal): " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {

        A a = new A();
        B b = new B();
        C c = new C();

        // 🔹 Without Thread (Sequential)
        System.out.println("----- WITHOUT THREAD -----");
        a.print();
        b.print();
        c.print();

        // 🔹 With Thread (Concurrent)
        System.out.println("----- WITH THREAD -----");
        a.start();
        b.start();
        c.start();
    }
}

'''

## assi-12


'''


class A extends Thread {

    public void run() {

        for (int i = 1; i <= 100; i++) {

            System.out.println("A: " + i);
        }
    }
}

class B extends Thread
 {

    public void run()
 {

        for (int i = 1; i <= 100; i++)
 {
            
System.out.println("B: " + i);
        
}
    }
}

class C extends Thread {

    public void run() {

        for (int i = 1; i <= 100; i++) {

            System.out.println("C: " + i);
        }
    }
}

public class Main {

    public static void main(String[] args) {

        A a = new A();
        B b = new B();
        C c = new C();

        try {
            a.start();
            a.join();   // wait until A finishes

            b.start();
            b.join();   // wait until B finishes

            c.start();
            c.join();   // wait until C finishes

        } 
catch (InterruptedException e) {

            System.out.println(e);
        }
    }
}

'''

## assi-13

'''

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        int sum = a + b;

        System.out.println("Result: " + sum);
    }
}

'''

## assi-14

'''

import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // 🔹 Taking 10 inputs (Registration Form)
        System.out.print("Enter Name: ");
        String name = sc.nextLine();

        System.out.print("Enter Email: ");
        String email = sc.nextLine();

        System.out.print("Enter Password: ");
        String password = sc.nextLine();

        System.out.print("Enter Gender: ");
        String gender = sc.nextLine();

        System.out.print("Enter Course: ");
        String course = sc.nextLine();

        System.out.print("Enter Address: ");
        String address = sc.nextLine();

        System.out.print("Enter Phone: ");
        String phone = sc.nextLine();

        System.out.print("Enter Age: ");
        String age = sc.nextLine();

        System.out.print("Enter City: ");
        String city = sc.nextLine();

        System.out.print("Enter State: ");
        String state = sc.nextLine();

        // 🔹 Display Data (Simulating Database Storage)
        System.out.println("\n--- Registration Data ---");
        System.out.println("Name: " + name);
        System.out.println("Email: " + email);
        System.out.println("Password: " + password);
        System.out.println("Gender: " + gender);
        System.out.println("Course: " + course);
        System.out.println("Address: " + address);
        System.out.println("Phone: " + phone);
        System.out.println("Age: " + age);
        System.out.println("City: " + city);
        System.out.println("State: " + state);

        System.out.println("\nData Stored Successfully (Simulated)");
    }
}

'''

## assi-14

```

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm extends JFrame implements ActionListener {

    JTextField name, email, phone, address, dob, course, city, pincode;
    JPasswordField password;
    JRadioButton male, female;
    JButton submit;

    public RegistrationForm() {

        setTitle("Registration Form");
        setSize(400, 600);
        setLayout(new GridLayout(12,2));

        add(new JLabel("Name:"));
        name = new JTextField();
        add(name);

        add(new JLabel("Email:"));
        email = new JTextField();
        add(email);

        add(new JLabel("Password:"));
        password = new JPasswordField();
        add(password);

        add(new JLabel("Gender:"));
        JPanel genderPanel = new JPanel();
        male = new JRadioButton("Male");
        female = new JRadioButton("Female");
        ButtonGroup bg = new ButtonGroup();
        bg.add(male);
        bg.add(female);
        genderPanel.add(male);
        genderPanel.add(female);
        add(genderPanel);

        add(new JLabel("Phone:"));
        phone = new JTextField();
        add(phone);

        add(new JLabel("Address:"));
        address = new JTextField();
        add(address);

        add(new JLabel("DOB (YYYY-MM-DD):"));
        dob = new JTextField();
        add(dob);

        add(new JLabel("Course:"));
        course = new JTextField();
        add(course);

        add(new JLabel("City:"));
        city = new JTextField();
        add(city);

        add(new JLabel("Pincode:"));
        pincode = new JTextField();
        add(pincode);

        submit = new JButton("Register");
        submit.addActionListener(this);
        add(submit);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {

        String userName = name.getText();
        String userEmail = email.getText();
        String userPass = new String(password.getPassword());
        String userGender = male.isSelected() ? "Male" : "Female";
        String userPhone = phone.getText();
        String userAddress = address.getText();
        String userDOB = dob.getText();
        String userCourse = course.getText();
        String userCity = city.getText();
        String userPincode = pincode.getText();

        try {
            Class.forName("com.mysql.cj.jdbc.Driver");

            Connection con = DriverManager.getConnection(
                "jdbc:mysql://localhost:3306/registration_db", "root", "password");

            String query = "INSERT INTO users(name,email,password,gender,phone,address,dob,course,city,pincode) VALUES(?,?,?,?,?,?,?,?,?,?)";

            PreparedStatement ps = con.prepareStatement(query);

            ps.setString(1, userName);
            ps.setString(2, userEmail);
            ps.setString(3, userPass);
            ps.setString(4, userGender);
            ps.setString(5, userPhone);
            ps.setString(6, userAddress);
            ps.setString(7, userDOB);
            ps.setString(8, userCourse);
            ps.setString(9, userCity);
            ps.setString(10, userPincode);

            ps.executeUpdate();

            JOptionPane.showMessageDialog(this, "Registration Successful!");

            con.close();

        } catch (Exception ex) {
            ex.printStackTrace();
        }
    }

    public static void main(String[] args) {
        new RegistrationForm();
    }
}

```
## assi-15

```

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class Calculator extends JFrame implements ActionListener {

    JTextField tf;
    JButton b[] = new JButton[16];
    String s[] = {"7","8","9","/",
                  "4","5","6","*",
                  "1","2","3","-",
                  "0","C","=","+"};

    double num1, num2, result;
    char operator;

    public Calculator() {

        setTitle("Calculator");
        setSize(300, 400);
        setLayout(new BorderLayout());

        tf = new JTextField();
        tf.setFont(new Font("Arial", Font.BOLD, 20));
        add(tf, BorderLayout.NORTH);

        JPanel p = new JPanel();
        p.setLayout(new GridLayout(4,4));

        for(int i=0;i<16;i++) {
            b[i] = new JButton(s[i]);
            b[i].setFont(new Font("Arial", Font.BOLD, 18));
            b[i].addActionListener(this);
            p.add(b[i]);
        }

        add(p, BorderLayout.CENTER);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {

        String str = e.getActionCommand();

        if(str.charAt(0) >= '0' && str.charAt(0) <= '9') {
            tf.setText(tf.getText() + str);
        }
        else if(str.charAt(0) == 'C') {
            tf.setText("");
        }
        else if(str.charAt(0) == '=') {
            num2 = Double.parseDouble(tf.getText());

            switch(operator) {
                case '+': result = num1 + num2; break;
                case '-': result = num1 - num2; break;
                case '*': result = num1 * num2; break;
                case '/': result = num1 / num2; break;
            }

            tf.setText("" + result);
        }
        else {
            num1 = Double.parseDouble(tf.getText());
            operator = str.charAt(0);
            tf.setText("");
        }
    }

    public static void main(String[] args) {
        new Calculator();
    }
}

```

## assi-16

```

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class MatrixAddition extends JFrame implements ActionListener {

    JTextField a[][] = new JTextField[2][2];
    JTextField b[][] = new JTextField[2][2];
    JTextField c[][] = new JTextField[2][2];

    JButton addBtn;

    public MatrixAddition() {

        setTitle("Matrix Addition");
        setSize(400, 300);
        setLayout(new GridLayout(4, 4));

        // Matrix A
        for(int i=0;i<2;i++) {
            for(int j=0;j<2;j++) {
                a[i][j] = new JTextField();
                add(a[i][j]);
            }
        }

        // Matrix B
        for(int i=0;i<2;i++) {
            for(int j=0;j<2;j++) {
                b[i][j] = new JTextField();
                add(b[i][j]);
            }
        }

        // Result Matrix C
        for(int i=0;i<2;i++) {
            for(int j=0;j<2;j++) {
                c[i][j] = new JTextField();
                c[i][j].setEditable(false);
                add(c[i][j]);
            }
        }

        addBtn = new JButton("Add");
        addBtn.addActionListener(this);
        add(addBtn);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {

        try {
            for(int i=0;i<2;i++) {
                for(int j=0;j<2;j++) {

                    int num1 = Integer.parseInt(a[i][j].getText());
                    int num2 = Integer.parseInt(b[i][j].getText());

                    int sum = num1 + num2;
                    c[i][j].setText(String.valueOf(sum));
                }
            }
        } catch(Exception ex) {
            JOptionPane.showMessageDialog(this, "Enter valid numbers!");
        }
    }

    public static void main(String[] args) {
        new MatrixAddition();
    }
}

```

## assi-17

```

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class ShapeDrawer extends JFrame implements ActionListener {

    JButton[] buttons = new JButton[10];
    String[] names = {
        "Circle", "Oval", "Rectangle", "Square", "Line",
        "Triangle", "Arc", "RoundRect", "Fill Circle", "Fill Rectangle"
    };

    String shape = "";

    public ShapeDrawer() {

        setTitle("Shape Drawer");
        setSize(600, 500);
        setLayout(new FlowLayout());

        // Create 10 buttons
        for (int i = 0; i < 10; i++) {
            buttons[i] = new JButton(names[i]);
            buttons[i].addActionListener(this);
            add(buttons[i]);
        }

        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        shape = e.getActionCommand(); // get clicked button name
        repaint(); // redraw frame
    }

    public void paint(Graphics g) {
        super.paint(g);

        g.setColor(Color.BLUE);

        int x = 200, y = 150;

        switch (shape) {

            case "Circle":
                g.drawOval(x, y, 100, 100);
                break;

            case "Oval":
                g.drawOval(x, y, 150, 80);
                break;

            case "Rectangle":
                g.drawRect(x, y, 150, 100);
                break;

            case "Square":
                g.drawRect(x, y, 100, 100);
                break;

            case "Line":
                g.drawLine(x, y, x + 150, y + 100);
                break;

            case "Triangle":
                g.drawLine(x, y, x + 80, y - 100);
                g.drawLine(x + 80, y - 100, x + 160, y);
                g.drawLine(x, y, x + 160, y);
                break;

            case "Arc":
                g.drawArc(x, y, 120, 100, 0, 180);
                break;

            case "RoundRect":
                g.drawRoundRect(x, y, 150, 100, 30, 30);
                break;

            case "Fill Circle":
                g.fillOval(x, y, 100, 100);
                break;

            case "Fill Rectangle":
                g.fillRect(x, y, 150, 100);
                break;
        }
    }

    public static void main(String[] args) {
        new ShapeDrawer();
    }
}
```
















        


