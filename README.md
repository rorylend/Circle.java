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

## What I Learned

Superclasses, subclasses, creating public methods

