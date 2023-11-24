# C# Documentation

## 1. Introduction

### 1.1 Intro to C# language

**Programming language**: A language that Humans use to communicate with machines. Without computer programs, we wouldn't have smartphones, websites, or even exploration in outer space.

- Summary
  - C# is a powerful OOP language developed by Micorsoft.
  - General Purpose: We can create mobile, web,desktop and game application.
  - we can built application on the Microsoft .NET platform.
  - Cross Platform Independent: Micorsoft .NET Core made sure C# is not more only for windows but for linux and MacOS well.
  - typed safe / statically typed language

C# (pronounced "C sharp") is a modern, object-oriented programming language developed by Microsoft. It is designed for building a variety of applications on the Microsoft .NET platform. C# is widely used for developing desktop applications, web applications, mobile apps, cloud-based services, and game development.

Key features and aspects of C# include:

1. **Object-Oriented:** C# is an object-oriented programming (OOP) language, supporting concepts such as classes, objects, encapsulation, inheritance, and polymorphism.

2. **Managed Code:** C# code is typically compiled into an intermediate language called Common Intermediate Language (CIL), and it runs on the Common Language Runtime (CLR), which provides features like memory management (garbage collection), exception handling, and security.

3. **Type-Safe:** C# is statically typed, which means that the type of a variable must be declared before it can be used. This helps catch type-related errors at compile time.

4. **Syntax:** C# syntax is influenced by languages like C, C++, and Java. If you are familiar with these languages, you'll find many similarities in C# syntax.

5. **Rich Standard Library:** C# comes with a comprehensive standard library, part of the .NET Framework or .NET Core, which provides functionality for tasks such as file I/O, networking, database access, and more.

6. **Integrated Development Environment (IDE):** Microsoft provides Visual Studio, a powerful IDE for C# development. Visual Studio offers features like code completion, debugging tools, and project management, making it a popular choice among C# developers.

7. **Cross-Platform Development:** With the introduction of .NET Core, C# is no longer limited to Windows development. .NET Core is a cross-platform, open-source framework that allows C# developers to build applications for Windows, Linux, and macOS.

8. **Language Features:** C# includes modern language features such as LINQ (Language-Integrated Query), async/await for asynchronous programming, properties, events, delegates, and more.

9. **Web Development:** C# is commonly used for web development, particularly in combination with ASP.NET, a framework for building web applications.

10. **Game Development:** C# is a primary language for game development using the Unity game engine. Unity enables developers to create games for various platforms, including desktop, mobile, and consoles.

C# continues to evolve with new features and improvements, and it remains a popular choice for developers building a wide range of applications in different domains.

### 1.2 Setting up the environment

- mac: install .NET Core using homebrew. `brew install --cask dotnet-sdk` and check the version `dotnet --version`
- install VSCode editior
- install c# extension

### 1.3 First C# Program

- output: a message on screen/terminal. `Console.WriteLine("Welcome to C#!");`

  ```c#
  using System;

  public class Program
  {
      public static void Main(string[] args)
      {
          Console.Write("Welcome to the Code Playground");
          Console.WriteLine("Welcome to the Code Playground");
      }
  }
  ```

#### break down basic structure

- Namespaces / Class: helps to separate code. `usng System;` allows you to use Console.WriteLine method and other methods. Namespaces are optional. Instead of System.Console.WriteLine use Console.WriteLine method by use System. Use . operator to access the class or namespace members.

- In C#, creating a class is mandatory for the program’s execution. Main method is the entry point or starting point of the program.

To run the first C# program in Visual Studio Code (VSCode), follow these steps:

#### Step 1: Install Required Software

1. **Install Visual Studio Code:**
   If you don't have Visual Studio Code installed, you can download and install it from the official website: [Visual Studio Code](https://code.visualstudio.com/).

2. **Install .NET SDK:**
   Ensure you have the .NET SDK installed on your machine. You can follow the previous instructions to install it using Homebrew on macOS.

#### Step 2: Set Up a C# Project

1. **Create a Folder:**
   Open your terminal and create a new folder for your C# project:

   ```bash
   mkdir HelloWorld
   cd HelloWorld
   ```

2. **Initialize a C# Project:**
   Run the following command to initialize a new C# console application:

   ```bash
   dotnet new console
   ```

   This command creates a simple "Hello World" C# console application.

#### Step 3: Open Project in Visual Studio Code

1. **Open VSCode:**
   Open Visual Studio Code and navigate to the folder you created for your C# project:

   ```bash
   code .
   ```

   This command opens the current folder in VSCode.

#### Step 4: Run the Program

1. **Open Terminal in VSCode:**
   In VSCode, open a new terminal by clicking on "View" in the top menu and selecting "Terminal."

2. **Build and Run:**
   In the terminal, run the following commands to build and run your C# program:

   ```bash
   dotnet build
   dotnet run
   ```

   This will build and execute your C# program. You should see the "Hello World" output in the terminal.

Congratulations! You've successfully run your first C# program in Visual Studio Code. You can now start exploring and writing C# code in your VSCode environment.

#### Statements

- A statement (a line of code) performs a specific task. Each Statement ends with a semicolon.
- In case of multiple statements top to bottom is the apporach of executing statements.

```c#
public class Program{
  public static void Main(string[] args)
  {
    Console.WriteLine("My name is Anisul Islam.");
    Console.WriteLine(143);
  }
}
```

#### Assignment 1: Print your bio

### 1.4 comments

- what is comment and why do you need comment?
      - to explain your code
      - to avoid running some part of your code for debugging
- single line comment -> `// this is a single line comment`
- multi-line comments -> `/*   */`

### 1.5 Variables and data types

- variable declaration and initialization
- data type
      - string; example of string: "this is a string"
         - `string name; name="Anisul Islam";`
      - char; char bloodGroup = 'A'
      - int; int age = 32
      - double; double age = 95.4
      - float height = 1.82f;
      - decimal weight = 92.8m;
      - bool isRegistered = true;

- we can change the value of variable anywhere in the program

#### variable naming conventions

#### Assignment 2: declare product data types and print variables

#### Constant variables and multiple variables

- constant variables: const string universityName = "Leading University";
- string concatenation: "anisul" + "islam"
- multiple variables: int x,y,z; x=y=z=50;

#### Type Casting - Implicit, Explicit

- Implicit (automatically - converting a smaller type to a larger type size): char -> int -> long -> float -> double
- Explicit (manually - converting a larger type to a smaller size type): double -> float -> long -> int -> char
- Type Conversion Methods: It is also possible to convert data types explicitly by using built-in methods, such as Convert.ToBoolean, Convert.ToDouble, Convert.ToString, Convert.ToInt32 (int) and Convert.ToInt64 (long)

### 1.6 User Input

- Console.ReadLine(), Convert.ToString(), Convert.ToBoolean(), Convert.ToInt32(), Convert.ToInt64() and Convert.ToChar(), Convert.ToDouble()

```c#
using System;
class Test
{
  public static void Main(string[] args)
  {
    string? studentName;
    int studentAge;

    Console.Write("Enter your name: ");
    studentName = Console.ReadLine();

    Console.Write("Enter your age: ");
    studentAge = Convert.ToInt32(Console.ReadLine());

    Console.WriteLine("Name: " + studentName);
    Console.WriteLine("Age: " + studentAge + " years old");
  }
}
```

#### Assignment 3: take student input for gpa and isRegistered

### 1.7 Math operatoions & Precedence

### 1.8 Formatting output

```c sharp
    int number1 = 10;
    int number2 = 3;
    int result;
    double pi = 3.1416;

    result = number1 + number2;
    // Console.WriteLine($"{number1} + {number2} = {result}");
    Console.WriteLine("{0} + {1} = {2}", number1, number2, result);

   Console.WriteLine($"pi = {pi}");
   Console.WriteLine($"pi = {pi.F2}");

```

### 1.9 Operators

C# supports various operators that allow you to perform operations on variables and values. Here's a list of some common operators in C#:

#### Arithmetic Operators

1. **Addition (`+`):**

   ```csharp
   int result = a + b;
   ```

2. **Subtraction (`-`):**

   ```csharp
   int result = a - b;
   ```

3. **Multiplication (`*`):**

   ```csharp
   int result = a * b;
   ```

4. **Division (`/`):**

   ```csharp
   int result = a / b;
   ```

5. **Modulus (`%`):**

   ```csharp
   int result = a % b;
   ```

- some arithmetic operators programs

```csharp
// basic calculator
using System;
class Test
{
  public static void Main(string[] args)
  {
    int number1 = 10;
    int number2 = 3;
    int result;

    result = number1 + number2;
    // Console.WriteLine($"{number1} + {number2} = {result}");
    Console.WriteLine("{0} + {1} = {2}", number1, number2, result);

    result = number1 - number2;
    Console.WriteLine($"{number1} - {number2} = {result}");

    result = number1 * number2;
    Console.WriteLine($"{number1} * {number2} = {result}");


    double div = (double)number1 / number2;
    Console.WriteLine($"{number1} / {number2} = {div.ToString("F2")}");


    result = number1 % number2;
    Console.WriteLine($"{number1} % {number2} = {result}");

  }
}

// area of triagle
using System;
class Test
{
  public static void Main(string[] args)
  {
    // triangle area = 0.5 * base * height
    double baseLength, height, triangleArea;

    Console.WriteLine("Triangle Area Calculator");

    Console.Write("Base = ");
    baseLength = Convert.ToDouble(Console.ReadLine());

    Console.Write("Height = ");
    height = Convert.ToDouble(Console.ReadLine());

    triangleArea = 0.5 * baseLength * height;
    Console.WriteLine($"Triangle Area = {triangleArea.ToString("F2")}");
  }
}


// temperature conversion (celsius to fahrenheit conversion)
using System;
class Test
{
  public static void Main(string[] args)
  {
    double fahrenheit, celsius;

    Console.Write("fahrenheit = ");
    fahrenheit = Convert.ToDouble(Console.ReadLine());

    celsius = (fahrenheit - 32) / 1.8;
    Console.WriteLine($"celsius = {celsius:F2} degrees");

  }
}

```

##### Assignment 4:sum and average of 3 numbers

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    int number1, number2, number3, sum;
    double average;

    Console.Write("number1 = ");
    number1 = Convert.ToInt32(Console.ReadLine());

    Console.Write("number2 = ");
    number2 = Convert.ToInt32(Console.ReadLine());

    Console.Write("number3 = ");
    number3 = Convert.ToInt32(Console.ReadLine());

    sum = number1 + number2 + number3;
    Console.WriteLine($"sum = {sum}");

    average = (double)sum / 3;
    Console.WriteLine($"average = {average.ToString("F2")}");

  }
}

```

##### Assignment 5: area of circle

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    // circle area = 3.1416 * radius * radius
    double radius, circleArea;

    Console.WriteLine("Circle Area Calculator");

    Console.Write("radius = ");
    radius = Convert.ToDouble(Console.ReadLine());

    circleArea = Math.PI * radius * radius;
    Console.WriteLine($"Circle Area = {circleArea.ToString("F2")}");
  }
}
```

##### Assignment 6: temperature converter (fahrenheit to celsius conversion)

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    double fahrenheit, celsius;

    Console.Write("celsius = ");
    celsius = Convert.ToDouble(Console.ReadLine());

    fahrenheit = (1.8 * celsius) + 32;
    Console.WriteLine($"fahrenheit = {fahrenheit:F2} degrees");

  }
}


```

#### Relational Operators

1. **Equal to (`==`):**

   ```csharp
   if (a == b)
   ```

2. **Not equal to (`!=`):**

   ```csharp
   if (a != b)
   ```

3. **Greater than (`>`):**

   ```csharp
   if (a > b)
   ```

4. **Less than (`<`):**

   ```csharp
   if (a < b)
   ```

5. **Greater than or equal to (`>=`):**

   ```csharp
   if (a >= b)
   ```

6. **Less than or equal to (`<=`):**

   ```csharp
   if (a <= b)
   ```

#### Logical Operators

1. **Logical AND (`&&`):**

   ```csharp
   if (condition1 && condition2)
   ```

2. **Logical OR (`||`):**

   ```csharp
   if (condition1 || condition2)
   ```

3. **Logical NOT (`!`):**

   ```csharp
   if (!condition)
   ```

#### Assignment Operators

1. **Assignment (`=`):**

   ```csharp
   int a = 10;
   ```

2. **Add and assign (`+=`):**

   ```csharp
   a += 5;  // equivalent to a = a + 5;
   ```

3. **Subtract and assign (`-=`):**

   ```csharp
   a -= 5;  // equivalent to a = a - 5;
   ```

4. **Multiply and assign (`*=`):**

   ```csharp
   a *= 2;  // equivalent to a = a * 2;
   ```

5. **Divide and assign (`/=`):**

   ```csharp
   a /= 2;  // equivalent to a = a / 2;
   ```

6. **Modulus and assign (`%=`):**

   ```csharp
   a %= 3;  // equivalent to a = a % 3;
   ```

#### Increment and Decrement Operators

1. **Increment (`++`):**

   ```csharp
   a++;
   ```

2. **Decrement (`--`):**

   ```csharp
   a--;
   ```

#### Conditional Operator (Ternary Operator)

```csharp
int result = (a > b) ? a : b;
```

This is a concise way to express an `if-else` statement.

These are some of the basic operators in C#. Understanding how to use these operators is fundamental to writing effective C# code.
