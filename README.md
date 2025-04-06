# AP-Assignment-3

Question :-  Implement method overloading for an AreaCalculator class that calculates the area of a circle, rectangle, and triangle.

Program :- 

public class AreaCalculator {

  
    public double calculateArea(double radius) {
        return 3.14 * radius * radius;
    }

    public double calculateArea(double length, double width) {
        return length * width;
    }

    public double calculateArea(double base, double height, boolean isTriangle) {
        if (isTriangle) {
            return 0.5 * base * height;
        }
        return -1; 
    }

    public static void main(String[] args) {
        AreaCalculator calculator = new AreaCalculator();

        double circleArea = calculator.calculateArea(5.0);
        double rectangleArea = calculator.calculateArea(4.0, 6.0);
        double triangleArea = calculator.calculateArea(3.0, 4.0, true);

        System.out.println("Area of Circle: " + circleArea);
        System.out.println("Area of Rectangle: " + rectangleArea);
        System.out.println("Area of Triangle: " + triangleArea);
    }
}


Output :- 

Area of Circle: 78.5
Area of Rectangle: 24.0
Area of Triangle: 6.0
