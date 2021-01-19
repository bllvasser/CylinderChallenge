# CylinderChallenge
package academy.learnprogrmming;

public class Circle {
    double radius;

    public Circle(double radius) {
        this.radius = radius;
        if (radius < 0) {
            radius = 0;
        }
    }

    public double getRadius() {
        return radius;
    }

    public double getArea() {
        return (radius * radius * Math.PI);

    }

}

package academy.learnprogrmming;

public class Cylinder extends Circle {
    double height;

    public Cylinder(double radius, double height) {
        super(radius);
        this.height = height;
        if (height < 0) {
            height = 0;
        }
    }

    public double getHeight() {
        return height;
    }

    public double getVolume() {
        double volume = getArea() * height;
        return volume;
    }
}

package academy.learnprogrmming;

public class Main {





    public static void main(String[] args) {

        Circle circle = new Circle(3.75);
        System.out. println("circle.radius= " + circle.getRadius());
        System.out. println("circle.area= " + circle.getArea());
        Cylinder cylinder = new Cylinder(5.55, 7.25);
        System.out.println("cylinder.radius= " + cylinder.getRadius());
        System.out.println("cylinder.height= " + cylinder.getHeight());
        System.out.println("cylinder.area= " + cylinder.getArea());
        System.out.println("cylinder.volume= " + cylinder.getVolume());

    }
}

"C:\Program Files\Java\jdk-15.0.1\bin\java.exe" "-javaagent:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\lib\idea_rt.jar=50539:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\bin" -Dfile.encoding=UTF-8 -classpath C:\Users\nadiy\IdeaProjects\CylinderChallenge\out\production\CylinderChallenge academy.learnprogrmming.Main
circle.radius= 3.75
circle.area= 44.178646691106465
cylinder.radius= 5.55
cylinder.height= 7.25
cylinder.area= 96.76890771219959
cylinder.volume= 701.574580913447

Process finished with exit code 0
