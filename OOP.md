# Introduction to Object-Oriented Programming (OOP)

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of **objects**, which can contain data and methods. OOP helps organize code in a way that models real-world entities and their interactions. C# is a popular language that supports OOP principles.

## Key Concepts

### 1. **Classes and Objects**
- **Class**: A blueprint for creating objects. It defines properties (data) and methods (functions) that the objects created from the class will have.
- **Object**: An instance of a class. It contains actual values and can perform actions defined by the class.

#### Example:
```csharp
// Define a class
public class Car
{
    // Properties
    public string Brand { get; set; }
    public string Model { get; set; }
    
    // Method
    public void Start()
    {
        Console.WriteLine($"{Brand} {Model} is starting.");
    }
}

// Create an object
Car myCar = new Car
{
    Brand = "Toyota",
    Model = "Corolla"
};

// Use the object
myCar.Start(); // Output: Toyota Corolla is starting.
```

### 2. **Encapsulation**
Encapsulation is the concept of wrapping data (fields) and methods (functions) into a single unit called a class. It restricts direct access to some of the object’s components, which can protect the integrity of the data.

- **Private**: Members of a class that cannot be accessed from outside the class.
- **Public**: Members of a class that can be accessed from outside the class.

#### Example:
```csharp
public class Person
{
    // Private field
    private string _name;

    // Public property
    public string Name
    {
        get { return _name; }
        set
        {
            if (!string.IsNullOrEmpty(value))
                _name = value;
        }
    }
}
```

### 3. **Inheritance**
Inheritance allows a class to inherit properties and methods from another class. This promotes code reusability and establishes a hierarchical relationship between classes.

- **Base Class**: The class that is inherited from.
- **Derived Class**: The class that inherits from the base class.

#### Example:
```csharp
// Base class
public class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal is eating.");
    }
}

// Derived class
public class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog is barking.");
    }
}

// Create an object of the derived class
Dog myDog = new Dog();
myDog.Eat(); // Output: Animal is eating.
myDog.Bark(); // Output: Dog is barking.
```

### 4. **Polymorphism**
Polymorphism allows objects of different classes to be treated as objects of a common base class. It enables a method to do different things based on the object it is acting upon.

- **Method Overloading**: Multiple methods with the same name but different parameters.
- **Method Overriding**: Redefining a base class method in a derived class.

#### Example:
```csharp
// Base class
public class Shape
{
    public virtual void Draw()
    {
        Console.WriteLine("Drawing a shape.");
    }
}

// Derived class
public class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle.");
    }
}

// Use polymorphism
Shape myShape = new Circle();
myShape.Draw(); // Output: Drawing a circle.
```

### 5. **Abstraction**
Abstraction involves hiding complex implementation details and showing only the necessary features of an object. It is achieved using abstract classes and interfaces.

- **Abstract Class**: A class that cannot be instantiated and may contain abstract methods that must be implemented by derived classes.
- **Interface**: A contract that defines methods and properties that implementing classes must provide.

#### Example:
```csharp
// Abstract class
public abstract class Shape
{
    public abstract void Draw();
}

// Implementing class
public class Rectangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a rectangle.");
    }
}
```

---

This overview of Object-Oriented Programming (OOP) provides a foundation for understanding and using OOP principles in C#.
