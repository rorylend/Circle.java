[Tester.java](https://github.com/user-attachments/files/31161786/Tester.java)

This repository includes multiple steps from creating the superclass (Circle.java), the subclass (Cylinder.java), and running these classes by creating objects and calling their methods.
The outputs are Circle and Cylinder data printed to the console.

# Circle.java
## Description

This superclass holds a radius and calculates diameter, circumference, and area. Used as the base class for Cylinder.java.
The input is the radius.
The outputs are diameter, circumference, area, and a formatted toString.

## Tech Stack

- Language: Java
- Tool/Library: Eclipse
  
### 🟢 Code

<details>
<summary>Click to expand code</summary>

```java
// Rory Lendzion
// CSC110
// 7/9/26
public class Circle {
   protected double radius;
   // Gets called when a Circle object is created. Initializes all variables
   public Circle()
   {
      radius = 0.0;
   }
   public Circle(double radius)
   {
      this.radius = radius;
   }
   // This method copies the argument passed into the parameter to
   // the protected variable radius
   public void setRadius(double r)
   {
      radius = r;
   }
   // This method returns the value of the protected member
   // variable radius.
   public double getRadius()
   {
      return radius;
   }
   // This method calculates and returns the diameter of a circle object
   public double calculateDiameter()
   {
      return radius * 2.0;
   }
   // This method calculates and returns the circumference of a circle
   // object
   public double calculateCircumference()
   {
      return radius * 2.0 * 3.1416;
   }
   // This method calculates and returns the Circle object's area.
   public double calculateArea()
   {
      return 3.1416 * Math.pow(radius, 2);
   }
   // This method displays all of the data associated with a Circle
   // object, formatted to 2 decimal places.
   public String toString()
   {
      // Output results
      String result = "\nThe circle data is\n" +
          String.format("        Radius: %.2f\n", radius) +
          String.format("      Diameter: %.2f\n", calculateDiameter()) +
          String.format(" Circumference: %.2f\n", calculateCircumference()) +
          String.format("          Area: %.2f", calculateArea());
      return result;
   }
}
```

</details>

# Cylinder.java
## Description

This subclass inherits radius, diameter, circumference, and area from Circle.java, and adds a length and volume calculation.
The inputs are radius and length.
The outputs are volume, and a formatted toString that includes Circle.java's data.

## Tech Stack

- Language: Java
- Tool/Library: Eclipse
  
### 🟢 Code

<details>
<summary>Click to expand code</summary>
  
```java
// Rory Lendzion
// CSC110
// 7/9/26

//class declaration
public class Cylinder extends Circle {

   private double length;

   //Sets radius (via super) and length to 0.0
   public Cylinder()
   {
      super();
      length = 0.0;
   }

   // Overloaded constructor. Accepts radius and length
   public Cylinder(double radius, double length)
   {
      super(radius);
      this.length = length;
   }

   // Mutator method for length.
   public void setLength(double length)
   {
      this.length = length;
   }
   
   // Accessor method for length.
   public double getLength()
   {
      return length;
   }
   
   // Calculates and returns the volume of the Cylinder object.
   public double calculateVolume()
   {
      return calculateArea() * length;
   }

   // Displays all of the data associated with a Cylinder object,
   // , formatted to 2 decimal places
   public String toString()
   {
      String result = super.toString() +
          "\nThe cylinder data is\n" +
          String.format("        Length: %.2f\n", length) +
          String.format("        Volume: %.2f", calculateVolume());

      return result;
   }
}
```
</details>

# Tester.java
## Description

This tests the Circle and Cylinder classes by creating objects and calling their methods. The outputs are Circle and Cylinder data printed to the console.

## Tech Stack

- Language: Java
- Tool/Library: Eclipse
  
### 🟢 Code

<details>
<summary>Click to expand code</summary>

```java
// Rory Lendzion
// CSC110
// 7/9/26

public class Tester {

   public static void main(String args[]) {

      // Define a Circle object.  Calls the default constructor
      Circle circle1 = new Circle();

      // set the radius of Circle object to 1.0
      circle1.setRadius(1.0);

      // Call Circle object's toString and display information
      System.out.println("CIRCLE1");
      System.out.println("-------");
      System.out.println(circle1);

      // Define a Cylinder object using the default constructor
      Cylinder cylinder1 = new Cylinder();

      System.out.println("\nCYLINDER1");
      System.out.println("---------");
      System.out.println(cylinder1);

      // Define a Cylinder object
      // radius is assigned to 5, length to 10
      Cylinder cylinder2 = new Cylinder(5.0, 10.0);

      // other code to show Cylinder object cylinder2 invoking different methods
      System.out.println("\nCYLINDER2");
      System.out.println("---------");
      System.out.println("Radius: " + cylinder2.getRadius());
      System.out.println("Length: " + cylinder2.getLength());
      System.out.println("Volume: " + cylinder2.calculateVolume());

      // code to show Cylinder object invoking toString method
      System.out.println(cylinder2);
   }
}
```
## Usage

Example input/output:
<details>
<summary>Click to expand code</summary>

```java
/* Expected output
 * 
 * CIRCLE1
   -------

   The circle data is
           Radius: 1.00
         Diameter: 2.00
    Circumference: 6.28
             Area: 3.14

   CYLINDER1
   ---------

   The circle data is
           Radius: 0.00
         Diameter: 0.00
    Circumference: 0.00
             Area: 0.00
   The cylinder data is
           Length: 0.00
           Volume: 0.00

   CYLINDER2
   ---------
   Radius: 5.0
   Length: 10.0
   Volume: 785.3999999999999

   The circle data is
           Radius: 5.00
         Diameter: 10.00
    Circumference: 31.42
             Area: 78.54
   The cylinder data is
           Length: 10.00
           Volume: 785.40
*/
```
</details>

## What I Learned

Superclasses, subclasses, creating public methods

