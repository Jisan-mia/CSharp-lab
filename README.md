
// triangle area program in C#
```csharp
using System;

class Test {
    static float findArea(float a, float b, float c) {
        if(a<0 || b<0 || c<0 || (a+b<=c) || (a+c <= b) || b+c<=a) {
            Console.Write("Not a valid triangle");
            System.Environment.Exit(0);
        }
        float s = (a + b + c) / 2;
        return (float)Math.Sqrt(s*(s-a)*(s-b)*(s-c));
    }
    
    public static void Main() {
        float a = 4.0f;
        float b = 5.0f;
        float c = 6.0f;
        Console.Write("Area is " + findArea(a,b,c));
    }
}
```

// Factorial program in C#
```csharp
using System;

namespace ConApp6
{
    class Program
    {
        static void Main(string[] args) 
        {
            int n = 6;
            double fact = 1;
            for(int i = 1; i <= 6; i++) 
            {
                fact = fact * i;
            }
            Console.Write("Factorial of {0} = {1} " , n, fact);
            
            Console.ReadLine();
        }
    }
}
```

// sum of natural numbers
```csharp
using System;

public class Exercise4
{
    public static void Main()
    {
        int i=5,n,sum=0;
        
        Console.Write("\n\n");
        Console.Write("Read N numbers and calculate sum: \n");
        Console.Write("---------------------------------");
        Console.Write("\n\n");
        
        Console.Write("Input the numbers : \n");
        while(i<=n)
        {
            Console.Write("Number-{0} :",i);
            n = Convert.ToInt32(Console.ReadLine());
            sum += n;
        }
        
        Console.Write("The sum of 10 is: {0}\n", sum);
    }
}
```


// inheritence program in C#
```csharp
using System;
public class Employee
{
    public float salary = 40000;
}
public class Programmer:Employee
{
    public float bonus = 10000;
}

class TestInheritence {
    public static void Main(string[] args) 
    {
        Programmer p1 = new Programmer();
        
        Console.WriteLine("Salary: " + p1.salary);
        Console.WriteLine("Bonus: " + p1.bonus);
    }
}
```


// max and min value of an array C#
```csharp
using System;

namespace ConsoleApp1
{
    class Program {
        static void Main() {
            int[] arr = new int[10] {1, 5, 3, 2, 8, 9, 15, 4, 7, 20} ;
            
            
            
            int max = arr[0];
            int min = arr[0];
            
            for(int i = 0; i<arr.Length; i++) {
                if(arr[i] > max) {
                    max = arr[i];
                }
                if(arr[i] < min) {
                    min = arr[i];
                }
            }
            
            Console.WriteLine("largest:" + max);
            Console.WriteLine("smallest:" + min);
            
        }
    }
}
```

// uses of interfeces in C#
```csharp
using System;

interface Vehicle {
    void changeGear(int a);
    void speedUp(int a);
    void applyBreak(int a);
}

class Bicycle: Vehicle
{
    int gear;
    int speed;
    
    public void changeGear(int newGear) {
        gear = newGear;
    }
    public void speedUp(int increment) {
        speed = speed + increment;
    }
    public void applyBreak(int decrement) {
        speed = speed - decrement;
    }
    public void printStats() {
        Console.WriteLine("speed: " + speed + " gear: " + gear);
    }
}

class Interf {
    public static void Main(string[] args) {
        Bicycle bicycle = new Bicycle();
        bicycle.changeGear(2);
        bicycle.speedUp(3);
        bicycle.applyBreak(2);
        Console.WriteLine("Bicycle present stats: ");
        bicycle.printStats();
    }
}
```

// multiple inhertence program in C#
```csharp
using System;
namespace inheritenceApp{
    class Shape{
        public void setWidth(int w) {
            width = w;
        }
        public void setHeight(int h) {
            height = h;
        }
        protected int width;
        protected int height;
    }
    
    public interface PaintCost {
        int getCost(int area);
    }
    
    class Rectangle: Shape, PaintCost {
        public int getArea() {
            return (width*height);
        }
        public int getCost(int area) {
            return area*70;
        }
    }
    
    class RectangleTester {
        static void Main(string[] args) {
            Rectangle Rect = new Rectangle();
            int area;
            
            Rect.setWidth(5);
            Rect.setHeight(7);
            area = Rect.getArea();
            
            Console.WriteLine("Total area: " + Rect.getArea());
            Console.WriteLine("total plain cost: ${0} ", Rect.getCost(area));
        }
    }
}
```

// 1 to n prime number
```csharp
using System;

class PrimeProgram {
    static bool isPrime(int n) {
        if(n == 1 || n == 0) return false;
        
        for(int i = 2; i < n; i++) {
            if(n%i == 0) return false;
        }
        return true;
    }
    
    public static void Main(String[] args){
        int N;
        Console.Write("Enter the ending number of the range: ");
        N = Convert.ToInt32(Console.ReadLine());
        
        for(int i = 1; i <= N; i++) {
            if(isPrime(i)) {
                Console.Write(i + " ");
            }
        }
    }
}
```


// factorial of n using recursion
```csharp
using System;

class FactorialOfN {
    static void Main() {
        decimal f;
        Console.Write("Input a number: ");
        int num = Convert.ToInt32(Console.ReadLine());
        f = factorial(num);
        Console.WriteLine("The factorial of {0}! is {1}", num, f);
    }
    static decimal factorial(int n) {
        if(n == 0) {
            return 1;
        } else {
            return n * factorial(n-1);
        }
    }
    
}
```
// root of quadratic equations
```csharp
using System;

public class qEquations {
    public static void Main() {
        int a,b,c;
        double d,x1,x2;
        
        Console.Write("Enter the value of a: ");
        a = Convert.ToInt32(Console.ReadLine());
        Console.Write("Enter the value of b: ");
        b = Convert.ToInt32(Console.ReadLine());
        Console.Write("Enter the value of c: ");
        c = Convert.ToInt32(Console.ReadLine());
        
        d = b*b - 4*a*c;
        
        if(d == 0) {
            Console.Write("Both roots are equal.\n");
            x1 = -b/(2.0*a);
            x2 = x1;
            
            Console.Write("First Root is= {0}\n", x1);
            Console.Write("Second Root is= {0}\n",x2);
        } 
        else if(d>0) {
            Console.Write("Boot roots are read and different-2\n");
            x1 = (-b+Math.Sqrt(d))/(2*a);
            x2 = (-b-Math.Sqrt(d))/(2*a);
            
            Console.Write("First Root is= " + x1);
            Console.Write("Second Root is= " + x2);
        } 
        else {
            Console.Write("Roots are imaginary\n No solution. \n");
        }

    }
}
```
// sum from 1-100 
```csharp
using System;
public class Exercise11 {
    public static void Main() {
        int sum = 0;
        for(int i = 1; i<=100; i++) {
            sum+=i;
        }
        Console.Write("The sum is: " + sum);
    }
}
```
// array value ascending order (iterative)
```csharp
using System;
class AscendingArr{
    public static void Main() {
        int[] arr = new int[] {2,5, 1,8,10,4,9,5,3,6};
        int temp;
        
        for(int i = 0; i < arr.Length; i++) {
            for(int j = i+1; j < arr.Length; j++) {
                if(arr[i] > arr[j]) {
                    temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
        
        foreach(int value in arr) {
            Console.Write(value + " ");
        }
    }
}
```
