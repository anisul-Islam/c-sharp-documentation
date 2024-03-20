# C# Documentation

## Table of Contents

1. [Basic C#]
   - [1. Intro to C#](#basic-1-introduction)
      - [Intro to C# language](#11-intro-to-c-sharp-language)  
      - [Setting up the environment](#12-setting-up-the-environment)  
      - [First C# Program](#13-create-first-console-application)  
      - [Comments and escape sequences](#14-comments-and-escape-sequences)  
      - [Variables and data types](#15-variables-and-data-types)  
      - [User Input](#16-user-input)  
      - [Math operatoions & Precedence](#17-math-operatoions--precedence)  
      - [Formatting output](#18-formatting-output---string-concatenation--interpolation)  
   - [2. Operators](#basic-2-operators)  
   - [3. Control Statement](#basic-3-control-statement)  
      - [Conditional Control Statement](#31-conditional-control-statement)  
      - [Loop Control Statement](#32-loop-control-statement)  
   - [4. Methods](#basic-4-methods--function)  


2. [Intermediate C]()
   - [Intermediate 1. OOP](#intermediate-1-oop)
      - [Class and Object](#classes-and-objects)
   - [Intermediate 1. OOP](#intermediate-1-oop)
3. [3. Advanced C](#basic-c)
   - []()

## Basic 1. Introduction

### 1.1 Intro to C-sharp language

#### 1.1.1 Programming language

A language that Humans use to communicate with machines. Without computer programs, we wouldn't have smartphones, websites, or even exploration in outer space. Low-level, mid-level and high level language.

#### 1.1.2 What is C#? Why C#?

C# (pronounced "C sharp") is a modern, object-oriented programming language developed by Microsoft. It is designed for building a variety of applications on the Microsoft .NET platform. C# is widely used for developing desktop applications, web applications, mobile apps, cloud-based services, and game development.

Key features and aspects of C# include:

1. **Object-Oriented:** C# is an object-oriented programming (OOP) language, supporting concepts such as classes, objects, encapsulation, inheritance, and polymorphism.

2. **Managed Code:** C# code is typically compiled into an intermediate language called Common Intermediate Language (CIL), and it runs on the Common Language Runtime (CLR), which provides features like memory management (garbage collection), exception handling, and security.

3. **Type-Safe:** C# is statically typed, which means that the type of a variable must be declared before it can be used. This helps catch type-related errors at compile time.

4. **Syntax:** C# syntax is influenced by languages like C, C++, and Java. If you are familiar with these languages, you'll find many similarities in C# syntax. C++ and Visual Basics = C#

5. **Rich Standard Library:** C# comes with a comprehensive standard library, part of the .NET Framework or .NET Core, which provides functionality for tasks such as file I/O, networking, database access, and more.

6. **Integrated Development Environment (IDE):** Microsoft provides Visual Studio, a powerful IDE for C# development. Visual Studio offers features like code completion, debugging tools, and project management, making it a popular choice among C# developers.

7. **Cross-Platform Development:** With the introduction of .NET Core, C# is no longer limited to Windows development. .NET Core is a cross-platform, open-source framework that allows C# developers to build applications for Windows, Linux, and macOS.

8. **Language Features:** C# includes modern language features such as LINQ (Language-Integrated Query), async/await for asynchronous programming, properties, events, delegates, and more.

9. **Web Development:** C# is commonly used for web development, particularly in combination with ASP.NET, a framework for building web applications.

10. **Game Development:** C# is a primary language for game development using the Unity game engine. Unity enables developers to create games for various platforms, including desktop, mobile, and consoles.

- Summary
  - C# is a powerful OOP language developed by Micorsoft.
  - General Purpose: We can create Console Application, windows form application, mobile application, web application, desktop and game application (2D/3D).
  - we can built application on the Microsoft .NET platform.
  - Cross Platform Independent: Micorsoft .NET Core made sure C# is not more only for windows but for linux and MacOS well.
  - typed safe / statically typed language

#### 1.1.3 [.NET Framework & .NET Core](https://www.javatpoint.com/vb-net-dot-net-framework-introduction)

![alt text](image-3.png)
[!dot net framework](images/NET.png)
![alt text](image-2.png)

- The .NET Framework is not only a language, but it is also a software and language neutral platform.
- 2 main components: CLR (Common Language Runtime) take care of execution our app or running apps; .NET Framework class Library provides reusable code
- NET Framework is a mature framework primarily used for Windows-based applications, while .NET Core is a modern, cross-platform framework optimized for cloud-native and containerized applications. With the release of .NET 5 (and later .NET 6), Microsoft unified the .NET platform, merging .NET Core and .NET Framework into a single, unified platform called .NET. This unified platform provides a consistent development experience across different platforms and environments.

- .NET Ecosystem = Language (c#, f#, VB) + Runtime (CLR/ CORE CLR), Librariers (BCL Functions Base Class Libraries: System is an example)
  - CLR = JVM
  - Nuget package manager = npm

### 1.2 Setting up the environment

- step 1: install .NET Core; for mac using homebrew. `brew install --cask dotnet-sdk` and check the version `dotnet --version` `dotnet --help` for any command use `dotnet command --help`

- step 2: install IDE: Visual Studio is the popular one.

Visual Studio Code (VS Code) and Visual Studio (VS) are both popular Integrated Development Environments (IDEs) used for software development, but they have some key differences:

  1. **VS Code (Visual Studio Code)**:
    - VS Code is a lightweight, open-source code editor developed by Microsoft.
    - It provides extensive support for various programming languages through extensions.
    - VS Code is highly customizable and has a vast ecosystem of extensions for additional features and functionalities.
    - VS Code is suitable for a wide range of development tasks, including web development, cloud development, and scripting.

  2. **Visual Studio (VS)**:
    - Visual Studio is a full-featured Integrated Development Environment (IDE) developed by Microsoft.
    - All the tools are already installed for development purpose. It provides comprehensive tools and features for various types of software development, including desktop applications, web applications, mobile applications, and cloud services.
    - Visual Studio includes powerful debugging tools, code analysis, and testing capabilities.
    - Visual Studio has built-in support for multiple programming languages and platforms, including C#, C++, .NET, and more.  
    - It offers extensive project and solution management features, making it suitable for large-scale enterprise development.

- step 3: some useful for .NET and c# extension

  When working with C# and .NET in Visual Studio Code on macOS, you'll want to install some extensions to enhance your development experience. Here are some essential extensions:

    1. **C# for Visual Studio Code**: This official extension provides support for C# syntax highlighting, debugging, and IntelliSense. It's essential for C# development in Visual Studio Code.
      - [C# for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)

    2. **.NET Core Test Explorer**: If you're writing unit tests with .NET Core, this extension allows you to run and debug your tests directly within Visual Studio Code.
      - [.NET Core Test Explorer](https://marketplace.visualstudio.com/items?itemName=formulahendry.dotnet-test-explorer)

    3. **NuGet Package Manager**: This extension allows you to manage NuGet packages directly within Visual Studio Code, making it easier to install, update, and remove packages.
      - [NuGet Package Manager](https://marketplace.visualstudio.com/items?itemName=jmrog.vscode-nuget-package-manager)

    4. **C# XML Documentation Comments**: This extension provides IntelliSense for XML documentation comments in C#, helping you write better-documented code.
      - [C# XML Documentation Comments](https://marketplace.visualstudio.com/items?itemName=k--kato.docomment)

    5. **C# Extensions**: This extension provides additional C# code snippets and tools to improve your productivity.
      - [C# Extensions](https://marketplace.visualstudio.com/items?itemName=jchannon.csharpextensions)

    6. **C# FixFormat**: This extension automatically formats your C# code according to configurable rules, ensuring consistent code style.
      - [C# FixFormat](https://marketplace.visualstudio.com/items?itemName=Leopotam.csharpfixformat)

    7. **Debugger for Unity**: If you're developing Unity games using C#, this extension allows you to debug Unity applications directly from Visual Studio Code.
      - [Debugger for Unity](https://marketplace.visualstudio.com/items?itemName=Unity.unity-debug)

    8. **Unity Code Snippets**: Another useful extension for Unity development, providing code snippets for common Unity-related tasks.
      - [Unity Code Snippets](https://marketplace.visualstudio.com/items?itemName=kleber-swf.unity-code-snippets)

    To install these extensions, you can open Visual Studio Code, navigate to the Extensions view by clicking on the square icon on the sidebar or by pressing `Cmd + Shift + X`, and search for each extension by name. Then, click on the extension and select "Install". Alternatively, you can install them from the links provided above.

- step 4: important commands: run `dotnet new list`
Here are some important .NET CLI (Command Line Interface) commands used in .NET development:

1. **dotnet new**: Creates a new project or file based on the specified template.
   - Example: `dotnet new console` creates a new console application.

2. **dotnet restore**: Restores the dependencies and tools of a project.
   - Example: `dotnet restore` restores the NuGet packages for a project.

3. **dotnet build**: Builds the project and its dependencies.
   - Example: `dotnet build` compiles the project into executable output.

4. **dotnet run**: Builds and runs the project.
   - Example: `dotnet run` compiles and executes the project's entry point.

5. **dotnet test**: Executes the tests in the project.
   - Example: `dotnet test` runs the unit tests in the project.

6. **dotnet publish**: Publishes the application for deployment.
   - Example: `dotnet publish -c Release -o ./publish` publishes the application to the specified output directory in Release mode.

7. **dotnet clean**: Cleans the output directory and intermediate build files.
   - Example: `dotnet clean` removes the build artifacts from the project directory.

8. **dotnet add reference**: Adds a project-to-project (P2P) reference to the project file.
   - Example: `dotnet add reference ../path/to/project.csproj` adds a reference to another project.

9. **dotnet ef**: Entity Framework Core command-line tools for database migrations and scaffolding.
   - Example: `dotnet ef migrations add InitialCreate` creates a new migration for the database.

10. **dotnet tool install**: Installs the specified .NET Core CLI tool.
    - Example: `dotnet tool install --global dotnet-ef` installs the Entity Framework Core CLI tool globally.

### 1.3 Create First Console Application

- run `dotnet new list` and explain all the templates
- then create a basic console application with `dotnet new console` or `dotnet new console -o FirstConsoleApp`
- discuss folder structure:
  - .csproj (configuraion of the project = kind of same as package.json; later on if we add any package it will keep the information of the packages that we install)
  - entry point is the .cs file
    - run the project: dotnet run (run once)
    - watch the output: dotnet watch (run after every changes you made)
    - test the project: dotnet test
    - add package to the project: dotnet add packageName
    - add library from [nuget.org](https://www.nuget.org/) - search http
  - When you build a .NET project, the compiler generates intermediate language (IL) code, which is then translated into native machine code by the Just-In-Time (JIT) compiler when the application runs. **The compiled binary files,** along with any necessary resource files, configuration files, and dependencies, are stored in the bin directory.
  - create a .gitignore file `bin/ obj/` push the code and get again after cloning by `dotnet run`
- **.NET Framework code execution process** ![alt text](image.png)
  - .dll is the byte code or intermediate language
  - you wont see the binary code as the JIT (Just In Time) do not expose cause durinf the running process it will keep the binary code in the memory. JIT can create the binary code based the OS and it made the platform independent.

- output: a message on screen/terminal. `Console.WriteLine("Welcome to C#!");`

  ```c#
  using System;

  public class Program
  {
      public static void Main(string[] args)
      {
          Console.Write("Welcome to the Code Playground");
          Console.WriteLine("Welcome to the Code Playground");
          Console.ReadKey();
      }
  }
  ```

- break down basic structure

- Namespaces / Class: helps to separate code. `using System;` allows you to use Console.WriteLine method and other methods. Namespaces are optional. Instead of System.Console.WriteLine use Console.WriteLine method by use System. Use . operator to access the class or namespace members.

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

```csharp
class Test
{
  public static void Main(string[] args)
  {
    Console.WriteLine("Name: Anisul Islam");
    Console.WriteLine("Age: 32");
    Console.WriteLine("Profession: Software developer");
  }
}
```

#### Naming conventions in Micorsoft ecosystem

Sure, here's a breakdown of which naming convention is commonly used for what purpose in the Microsoft ecosystem:

1. **PascalCase**:
   - Class names: Used for naming classes and types. Example: `CustomerService`, `HttpRequest`.
   - Method names: Used for naming methods and functions. Example: `CalculateTotal`, `SendEmail`.
   - Property names: Used for naming properties of classes and objects. Example: `FirstName`, `TotalAmount`.

2. **camelCase**:
   - Variable names: Used for naming variables, parameters, and local variables. Example: `totalAmount`, `numberOfItems`.
   - Method parameter names: Used for naming parameters of methods and functions. Example: `firstName`, `orderId`.
   - undesrcore followed by camelCase for private instance.

3. **snake_case**:
   - File names: Used for naming files in some cases, particularly in web development. Example: `index.html`, `user_profile.css`.
   - Database identifiers: Used for naming database tables, columns, and stored procedures in some cases. Example: `user_profile`, `order_details`.

4. **Hungarian notation**:
   - Less commonly used in modern development but may still be found in legacy codebases. Example: `strFirstName` for a string variable holding a first name, `intAge` for an integer variable holding an age.

5. **Abbreviations**:
   - Used for common terms and concepts, especially in APIs and libraries. Example: `IO` for Input/Output, `HTTP` for Hypertext Transfer Protocol.

6. **Acronyms**:
   - Used for abbreviations and initialisms. Example: `HTML` for Hypertext Markup Language, `JSON` for JavaScript Object Notation.

7. **Namespaces and Assemblies**:
   - Namespaces and assemblies generally follow PascalCase and may include a reverse domain name. Example: `System.Collections`, `Microsoft.AspNetCore.Mvc`.

8. **Constants**:
   - Constants are typically named using PascalCase with all uppercase letters. Example: `MAX_VALUE`, `DEFAULT_TIMEOUT`.

These conventions help maintain consistency and readability across codebases, making it easier for developers to understand and maintain the code. However, it's essential to follow the specific naming guidelines of the project or organization you're working on.

### 1.4 comments and escape sequences

- what is comment and why do you need comment?
      - to explain your code
      - to avoid running some part of your code for debugging
- single line comment -> `// this is a single line comment`
- multi-line comments -> `/*   */`
- escape sequences: \n, \t, \r, \\, \", \'

```csharp
   string fullName = "Aniul\nIslam\nRubel";
   Console.WriteLine(fullName);
```

- verbatim string: it allows linebreaks in strings. use @ symbol before double quotes.

```csharp
Console.WriteLine(@"Hello!
Welcome to the verbatim string");
```

### 1.5 Variables and data types

- variable declaration and initialization

#### Data type

![alt text](image-1.png)

- 2 main type: Built-in: Value Types, Reference Type, User Defined
- example
  - string; example of string: "this is a string" `string name; name="Anisul Islam";`
  - char; char bloodGroup = 'A'
  - int; int age = 32
  - double; double age = 95.4
  - float height = 1.82f;
  - decimal weight = 92.8m;
  - bool isRegistered = true;
  - DateTime (8 bytes) - value range from 0:00:00 on 1/1/2001 to 23:59:59 on 12/31/9999

C# provides several built-in data types, which can be categorized into the following groups:

1. **Value Types**:
   - **Integral Types**: Represent whole numbers without a fractional component.
     - `sbyte`: 8-bit signed integer (-128 to 127)
     - `byte`: 8-bit unsigned integer (0 to 255)
     - `short`: 16-bit signed integer (-32,768 to 32,767)
     - `ushort`: 16-bit unsigned integer (0 to 65,535)
     - `int`: 32-bit signed integer (-2,147,483,648 to 2,147,483,647)
     - `uint`: 32-bit unsigned integer (0 to 4,294,967,295)
     - `long`: 64-bit signed integer (-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
     - `ulong`: 64-bit unsigned integer (0 to 18,446,744,073,709,551,615)
   - **Floating-Point Types**: Represent numbers with fractional parts.
     - `float`: 32-bit single-precision floating-point type
     - `double`: 64-bit double-precision floating-point type
     - `decimal`: 128-bit decimal type for financial and monetary calculations
   - **Other Value Types**:
     - `char`: 16-bit Unicode character
     - `bool`: Represents Boolean values (true or false)
     - struct : for small amount of data instead of class
     - enum
     - tuple : for stroing different realted data types in a single object
     - Nullable

2. **Reference Types**:
   - **Class**: Defines a reference type.
   - **Interface**: Defines a contract for classes to implement.
   - **Delegate**: Defines a reference to a method.
   - **Array**: Represents a collection of elements.
   - **String**: Represents a sequence of characters.
   - **Object**: The base class for all other types.

3. **Pointer Types** (Unsafe Code):
   - Allow direct memory manipulation and are rarely used in typical C# programming.

4. **DateTime**
   - DateTime (8 bytes) - value range from 0:00:00 on 1/1/2001 to 23:59:59 on 12/31/9999

C# also allows user-defined data types through the use of structures (`struct`) and enumerations (`enum`).

Here's an example demonstrating the declaration of variables with different data types:

```csharp
using System;

class Program
{
    static void Main()
    {
        // Integral Types
        sbyte sb = -100;
        byte b = 200;
        short sh = -30000;
        ushort ush = 60000;
        int i = -2000000000;
        uint ui = 4000000000;
        long l = -9000000000000000000;
        ulong ul = 18000000000000000000;

        // Floating-Point Types
        float f = 3.14f;
        double d = 3.14159265359;
        decimal dec = 123.45m;

        // Other Value Types
        char ch = 'A';
        bool flag = true;

        // Reference Types
        string str = "Hello, world!";
        object obj = 123;

        Console.WriteLine("Variables declared with different data types:");
        Console.WriteLine($"sbyte: {sb}");
        Console.WriteLine($"byte: {b}");
        Console.WriteLine($"short: {sh}");
        Console.WriteLine($"ushort: {ush}");
        Console.WriteLine($"int: {i}");
        Console.WriteLine($"uint: {ui}");
        Console.WriteLine($"long: {l}");
        Console.WriteLine($"ulong: {ul}");
        Console.WriteLine($"float: {f}");
        Console.WriteLine($"double: {d}");
        Console.WriteLine($"decimal: {dec}");
        Console.WriteLine($"char: {ch}");
        Console.WriteLine($"bool: {flag}");
        Console.WriteLine($"string: {str}");
        Console.WriteLine($"object: {obj}");
    }
}
```

- **structure type**

for simple data structure such as storing colors, pints, coordinates. similar to classes but they have differences in many aspectes.

In C#, a structure (struct) is a value type data type that allows you to encapsulate related data members and behaviors. Similar to classes, structures can have fields, properties, methods, and constructors. However, there are some key differences between classes and structures:

1. **Memory Allocation**:
   - Objects of classes are allocated memory on the heap, while instances of structures are allocated memory on the stack.
   - This difference in memory allocation can lead to performance benefits for structures, especially for small, frequently used data types.

2. **Inheritance**:
   - Structures cannot inherit from other structures or classes.
   - They cannot serve as base types for other structures or classes.

3. **Default Constructor**:
   - Structures always have an implicit default parameterless constructor, which initializes all fields to their default values.

4. **Copy Semantics**:
   - When you pass a structure to a method or assign it to another variable, the entire structure is copied. This contrasts with classes, where only a reference to the object is copied.

5. **Boxing and Unboxing**:
   - Structures are value types, and they do not require boxing and unboxing when used in certain contexts. This can improve performance in scenarios where boxing and unboxing are frequent.

Here's a basic example of a structure in C#:

```csharp
using System;

public struct Point
{
    // Fields
    public int X;
    public int Y;

    // Constructor
    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }

    // Method
    public void Display()
    {
        Console.WriteLine($"Point coordinates: ({X}, {Y})");
    }
}

class Program
{
    static void Main()
    {
        // Creating an instance of the Point structure
        Point point = new Point(10, 20);

        // Accessing fields and calling method
        Console.WriteLine($"X coordinate: {point.X}");
        Console.WriteLine($"Y coordinate: {point.Y}");
        point.Display();
    }
}
```

In this example, `Point` is a structure that represents a point in 2D space. It has two fields `X` and `Y`, a constructor to initialize these fields, and a method `Display()` to print the coordinates of the point.

- **tuple type**

A tuple in C# is a data structure that allows you to store a fixed-size collection of heterogeneous elements (i.e., elements of different data types) in a single object. Tuples provide a convenient way to group together related data without the need to define a custom class or structure explicitly.

Here's a basic example of how to use tuples in C#:

```csharp
using System;

class Program
{
    static void Main()
    {
        // Creating a tuple
        var person = Tuple.Create("John", 30, true);

        // Accessing tuple elements
        Console.WriteLine($"Name: {person.Item1}");
        Console.WriteLine($"Age: {person.Item2}");
        Console.WriteLine($"IsEmployed: {person.Item3}");

        // Updating tuple elements (not allowed, tuples are immutable)
        // person.Item1 = "Alice"; // This will result in a compile-time error

        // Deconstructing a tuple
        (string name, int age, bool isEmployed) = person;
        Console.WriteLine($"Name: {name}, Age: {age}, IsEmployed: {isEmployed}");
    }
}
```

In this example:

- We create a tuple `person` containing three elements: a string representing the person's name, an integer representing their age, and a boolean indicating whether they are employed.
- We access tuple elements using the `Item1`, `Item2`, and `Item3` properties of the tuple object.
- We demonstrate how to deconstruct a tuple into individual variables using the C# deconstruction syntax `(string name, int age, bool isEmployed) = person`.

Starting from C# 7.0, you can also use named tuples, which provide more expressive code by giving names to the elements of the tuple. Here's how you can use named tuples:

```csharp
using System;

class Program
{
    static void Main()
    {
        // Creating a named tuple
        var person = (Name: "John", Age: 30, IsEmployed: true);

        // Accessing named tuple elements
        Console.WriteLine($"Name: {person.Name}");
        Console.WriteLine($"Age: {person.Age}");
        Console.WriteLine($"IsEmployed: {person.IsEmployed}");

        // Deconstructing a named tuple
        (string name, int age, bool isEmployed) = person;
        Console.WriteLine($"Name: {name}, Age: {age}, IsEmployed: {isEmployed}");
    }
}
```

In this example, we define a tuple with named elements `Name`, `Age`, and `IsEmployed`, making the code more readable and self-explanatory. We then access these named elements directly using their names.

- dynamic and object type
In C#, both `dynamic` and `object` are used to handle situations where the type of an object is not known at compile time. However, they have different behaviors and use cases:

1. **`dynamic`**:
   - The `dynamic` keyword is used to declare a type that can hold any type of value at runtime.
   - It defers type checking until runtime rather than compile time.
   - It allows you to perform operations on objects without explicit type casting.
   - It provides late binding, meaning method calls and property accesses are resolved at runtime.
   - Example:

     ```csharp
      using System;

      class Program
      {
          static void Main(string[] args)
          {
              // Example using object type
              object obj = 10;
              Console.WriteLine($"Object value: {obj}"); // Output: Object value: 10

              int intValue = (int)obj; // Explicit casting
              Console.WriteLine($"Int value: {intValue}"); // Output: Int value: 10

              // Example using dynamic type
              dynamic dynamicVariable = 10;
              Console.WriteLine($"Dynamic variable: {dynamicVariable}"); // Output: Dynamic variable: 10

              dynamicVariable = "Hello";
              Console.WriteLine($"Dynamic variable: {dynamicVariable}"); // Output: Dynamic variable: Hello

              dynamicVariable = DateTime.Now;
              Console.WriteLine($"Dynamic variable: {dynamicVariable}"); // Output: Dynamic variable: [current datetime]
          }
      }

     ```

2. **`object`**:
   - The `object` type is a reference type that represents the base type of all other types in C#.
   - It can hold any type of value but requires explicit casting to access its members or convert it to another type.
   - It is a compile-time construct and doesn't provide late binding like `dynamic`.
   - It is typically used when you need to work with values of different types in a homogeneous collection or when the specific type is not known at compile time.
  
In summary, `dynamic` is used for late binding and dynamic behavior at runtime, while `object` is used for static typing and type safety at compile time. Choose between them based on your specific requirements and whether you need dynamic or static typing in your code.

- record and a delegate:

    1. **Record**: (use record / struct / class based on your need)
      Records are a feature introduced in C# 9.0 that provide a concise syntax for creating immutable data types. Records are primarily used for modeling data and are especially useful for DTOs (Data Transfer Objects), entities, and other types where immutability and equality are important.

    ```csharp
    using System;

    // Example of a record
    public record Person(string FirstName, string LastName, int Age);

    class Program
    {
        static void Main()
        {
            // Creating an instance of the record
            var person = new Person("John", "Doe", 30);

            // Accessing properties
            Console.WriteLine($"Name: {person.FirstName} {person.LastName}, Age: {person.Age}");
        }
    }
    ```

    In the above example:

  - We define a `Person` record with properties `FirstName`, `LastName`, and `Age`.
  - Records automatically generate a constructor, properties, `Equals()` method, `GetHashCode()` method, and `ToString()` method based on their members.
  - We create an instance of the `Person` record and access its properties.

2. **Delegate**:
   Delegates are used to define references to methods. They are similar to function pointers in C++ or function types in other languages. Delegates are especially useful for implementing events, callbacks, and LINQ queries.

    ```csharp
    using System;

    // Example of a delegate
    public delegate void MyDelegate(string message);

    class Program
    {
        static void Main()
        {
            // Creating an instance of the delegate
            MyDelegate myDelegate = DisplayMessage;

            // Invoking the delegate
            myDelegate("Hello, delegates!");

            // Multicast delegate
            myDelegate += DisplayAnotherMessage;
            myDelegate("Hello again!");
        }

        static void DisplayMessage(string message)
        {
            Console.WriteLine($"Message: {message}");
        }

        static void DisplayAnotherMessage(string message)
        {
            Console.WriteLine($"Another message: {message}");
        }
    }
    ```

    In the above example:

    - We define a delegate `MyDelegate` that points to methods accepting a `string` parameter and returning `void`.
    - We create an instance of the delegate and assign it to a method `DisplayMessage`.
    - We invoke the delegate, which in turn invokes the `DisplayMessage` method.
    - We demonstrate a multicast delegate by adding another method to the delegate invocation list using `+=`. When the delegate is invoked, both methods are called in the order they were added.

    These examples showcase the usage of records for immutable data types and delegates for method references and event handling in C#.

#### Class vs Struct vs Record

Key Differences:

- Classes are reference types with full support for inheritance and customization, while structs and records are value types with limited or no inheritance capabilities.
- Structs are primarily used for small, single-value data types and are passed by value, while records provide a concise syntax for defining immutable data types with value semantics.
- Records automatically generate boilerplate code for immutability and value equality, reducing developer overhead and potential sources of errors.
In summary, choose the appropriate type (class, struct, or record) based on the specific requirements of your application, considering factors such as mutability, inheritance, memory usage, and performance.

Sure, let's create an example to demonstrate the differences between classes, structs, and records.

**Example**:

Suppose we want to define a data type to represent a 2D point with X and Y coordinates. We'll create implementations using a class, a struct, and a record to showcase their differences.

1. **Class Implementation**:

   ```csharp
   public class PointClass
   {
       public int X { get; set; }
       public int Y { get; set; }

       public PointClass(int x, int y)
       {
           X = x;
           Y = y;
       }
   }
   ```

2. **Struct Implementation**:

   ```csharp
   public struct PointStruct
   {
       public int X { get; }
       public int Y { get; }

       public PointStruct(int x, int y)
       {
           X = x;
           Y = y;
       }
   }
   ```

3. **Record Implementation**:

   ```csharp
   public record PointRecord(int X, int Y);
   ```

Now, let's demonstrate the differences by creating instances of each type and modifying them:

```csharp
class Program
{
    static void Main(string[] args)
    {
        // Creating instances
        var classPoint = new PointClass(10, 20);
        var structPoint = new PointStruct(30, 40);
        var recordPoint = new PointRecord(50, 60);

        // Modifying values
        classPoint.X = 100; // Allowed because classes are mutable
        // structPoint.X = 200; // Error: Cannot modify readonly members in structs
        // recordPoint.X = 300; // Error: Records are immutable

        // Displaying values
        Console.WriteLine($"Class Point: ({classPoint.X}, {classPoint.Y})");
        Console.WriteLine($"Struct Point: ({structPoint.X}, {structPoint.Y})");
        Console.WriteLine($"Record Point: ({recordPoint.X}, {recordPoint.Y})");
    }
}
```

**Output**:

```
Class Point: (100, 20)
Struct Point: (30, 40)
Record Point: (50, 60)
```

**Explanation**:

- We can modify the `X` and `Y` properties of the `PointClass` instance because classes are mutable.
- In the `PointStruct` instance, we cannot modify the `X` and `Y` properties directly because structs are immutable. Attempting to do so will result in a compilation error.
- Similarly, the `PointRecord` instance is also immutable, so we cannot modify its properties directly. Any attempt to do so will result in a compilation error.

This example illustrates the differences in mutability between classes, structs, and records in C#. Classes are mutable, structs are usually immutable (except for methods that explicitly modify them), and records are immutable by default.

#### checking data type of a variable

```csharp
using System;

class Program
{
    static void Main()
    {
        int intValue = 10;
        double doubleValue = 10.5;
        string stringValue = "Hello";

        // Checking data types
        Console.WriteLine("Data type of intValue: " + intValue.GetType());
        Console.WriteLine("Data type of doubleValue: " + doubleValue.GetType());
        Console.WriteLine("Data type of stringValue: " + stringValue.GetType());
    }
}

```

#### variable naming conventions

- descriptive
- meaningful
- camelCase
- avoid single letter naming (exception for loops)

#### var vs int

In the provided code example, `var` is used instead of `int` for the loop variable because the loop variable is inferred from the type of the collection being iterated over. In this case, `Enumerable.Range(0, numbers.Length)` returns an `IEnumerable<int>`, so the loop variable will be of type `int`.

Using `var` allows the compiler to determine the type of the loop variable automatically based on the context, which can make the code cleaner and more concise. It's especially useful when dealing with complex types or when the type name is long and repetitive.

Here's the same code with `int` explicitly specified:

```csharp
foreach (int index in Enumerable.Range(0, numbers.Length))
{
    Console.WriteLine($"Index: {index}, Value: {numbers[index]}");
}
```

Both versions of the code will work identically, but using `var` can sometimes make the code more readable and maintainable.

#### Assignment 2: declare product data types and print variables

![assignment-2](images/assignment-2.png)

#### Constant variables and multiple variables

- constant variables: const string universityName = "Leading University";
- string concatenation: "anisul" + "islam"
- multiple variables: int x,y,z; x=y=z=50;

#### Type Casting - Implicit, Explicit

- Implicit (automatically - converting a smaller type to a larger type size): byte -> short -> int -> long -> float -> double
  - only supported for numeric values not for character or boolean
  - no need to write additional codes normally
- Explicit (manually - converting a larger type to a smaller size type): double -> float -> long -> int -> short -> byte
  - we need to write additional codes to do explicit type casting. 2 ways : by using cast operator or Convert class
  - all types can be converted to string using ToString()

  ```c-sharp
    double number = 50.5;
    int number2 = (int) number; // cast operator
    int number2 = Convert.ToInt32(number);
    string s = number2.ToString();
  ```

- Type Conversion Methods: Use int.Parse() or Convert.ToInt32(). It is also possible to convert data types explicitly by using built-in methods, such as Convert.ToBoolean, Convert.ToDouble, Convert.ToString, Convert.ToInt32 (int) and Convert.ToInt64 (long)
- `System.Console.WriteLine($"{number2.GetType()}");`

### 1.6 User Input

- Console.ReadLine() return a string,
- Console.Read() - Keep in mind that Console.Read() only reads a single character, so if you enter a string, it will only read the first character of that string. It returns an integer representing the Unicode value of the character read.
- For Data Type conversion
  - Convert.ToString(), Convert.ToBoolean(), Convert.ToInt16(),Convert.ToInt32(), Convert.ToInt64() and Convert.ToChar(), Convert.ToDouble()
- Error: not possible to convert a textual string like "welcome" to an int.

```c#
using System;
class Test
{
  public static void Main(string[] args)
  {
    string? studentName;
    int studentAge;
    double salary;

    Console.Write("Enter your name: ");
    studentName = Console.ReadLine();

    Console.Write("Enter your age: ");
    studentAge = Convert.ToInt32(Console.ReadLine());

    Console.Write("Enter your monthly salary: ");
    salary = Convert.ToDouble(Console.ReadLine());


    Console.WriteLine("Name: " + studentName);
    Console.WriteLine("Age: " + studentAge + " years old");
    Console.WriteLine($"Welcome {name}. You are {age}. Your salary is ${salary:F2}");
  }
}
```

#### Assignment 3: take student input for gpa and isRegistered

### 1.7 Math operatoions & Precedence

### 1.8 Formatting output - String concatenation & interpolation

- we can use variable inside a string by using string interpolation!

```c sharp
    int number1 = 10;
    int number2 = 3;
    int result;
    double pi = 3.1416;

    result = number1 + number2;
    // Console.WriteLine($"{number1} + {number2} = {result}");
    Console.WriteLine("{0} + {1} = {2}", number1, number2, result);

   Console.WriteLine($"pi = {pi}");
   Console.WriteLine($"pi = {pi:F2}");

```

## Basic 2. Operators

C# supports various operators that allow you to perform operations on variables and values. Here's a list of some common operators in C#:

### Arithmetic Operators

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
    Console.WriteLine($"{number1} / {number2} = {div:F2}");


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

#### Assignment 4: sum and average of 3 numbers

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

### Assignment Operators

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

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    int number = 20;

    number += 5; // number = number + 5
    Console.WriteLine($"{number}");

    number -= 5; // number = number - 5
    Console.WriteLine($"{number}");

    number *= 5; // number = number * 5
    Console.WriteLine($"{number}");

    number /= 5; // number = number / 5
    Console.WriteLine($"{number}");

    number %= 5; // number = number % 5
    Console.WriteLine($"{number}");

  }
}

```

### Relational Operators

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

### Logical Operators

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

### Bitwise Operators

In C#, bitwise operators perform operations at the bit level. These operators work with individual bits of integer types (`int`, `long`, `short`, `byte`, etc.). Here are the bitwise operators in C#:

1. **Bitwise AND (`&`):**
   - **Description:** Sets each bit to 1 if both bits are 1.
   - **Example:**

     ```csharp
     int result = 5 & 3;  // Binary: 101 & 011 = 001
     Console.WriteLine(result);  // Output: 1
     ```

2. **Bitwise OR (`|`):**
   - **Description:** Sets each bit to 1 if at least one of the corresponding bits is 1.
   - **Example:**

     ```csharp
     int result = 5 | 3;  // Binary: 101 | 011 = 111
     Console.WriteLine(result);  // Output: 7
     ```

3. **Bitwise XOR (`^`):**
   - **Description:** Sets each bit to 1 if only one of the corresponding bits is 1.
   - **Example:**

     ```csharp
     int result = 5 ^ 3;  // Binary: 101 ^ 011 = 110
     Console.WriteLine(result);  // Output: 6
     ```

4. **Bitwise NOT (`~`):**
   - **Description:** Inverts each bit.
   - **Example:**

     ```csharp
     int result = ~5;  // Binary: ~0101 = 1010
     Console.WriteLine(result);  // Output: -6
     ```

5. **Left Shift (`<<`):**
   - **Description:** Shifts the bits of a number to the left by a specified number of positions.
   - **Example:**

     ```csharp
     int result = 5 << 2;  // Binary: 101 << 2 = 10100
     Console.WriteLine(result);  // Output: 20
     ```

6. **Right Shift (`>>`):**
   - **Description:** Shifts the bits of a number to the right by a specified number of positions.
   - **Example:**

     ```csharp
     int result = 5 >> 1;  // Binary: 101 >> 1 = 10
     Console.WriteLine(result);  // Output: 2
     ```

Bitwise operators are commonly used in scenarios where individual bits represent flags or options, and you need to perform operations at a lower level than regular arithmetic operators.

### Increment and Decrement Operators

1. **Increment (`++`):**

   ```csharp
   a++;
   ```

2. **Decrement (`--`):**

   ```csharp
   a--;
   ```

### Conditional Operator (Ternary Operator)

```csharp
int result = (a > b) ? a : b;

// even/odd program
class Test
{
  public static void Main(string[] args)
  {
    Console.Write("Enter a number: ");
    int number = Convert.ToInt32(Console.ReadLine());

    string result = number % 2 == 0 ? "Even" : "Odd";
    Console.WriteLine($"{number} is an {result} number");
    Console.Read();
  }
}
```

This is a concise way to express an `if-else` statement.

These are some of the basic operators in C#. Understanding how to use these operators is fundamental to writing effective C# code.

## Basic 3. Control Statement

### 3.1 Conditional control statement

Control statements in C# are used to control the flow of execution in a program. They allow you to make decisions, loop through code, and execute different blocks of code based on certain conditions. Here are some of the main control statements in C#:

1. **if Statement:**
   - The `if` statement is used for conditional branching. It executes a block of code if a specified condition is true.

     ```csharp
     if (condition)
     {
         // Code to be executed if the condition is true
     }
     ```

   - nested if

2. **else Statement:**
   - The `else` statement is used with `if` to execute a block of code if the `if` condition is false.

     ```csharp
     if (condition)
     {
         // Code to be executed if the condition is true
     }
     else
     {
         // Code to be executed if the condition is false
     }
     ```

3. **else if Statement:**
   - The `else if` statement is used to specify a new condition to test if the previous `if` or `else if` conditions are false.

     ```csharp
     if (condition1)
     {
         // Code to be executed if condition1 is true
     }
     else if (condition2)
     {
         // Code to be executed if condition2 is true
     }
     else
     {
         // Code to be executed if all conditions are false
     }
     ```

4. **switch Statement:**
   - 4 keywords to remember: switch, case, break and default. The `switch` statement is used to select one of many code blocks to be executed.

     ```csharp
     switch (variable)
     {
         case value1:
             // Code to be executed if variable equals value1
             break;
         case value2:
             // Code to be executed if variable equals value2
             break;
         // ... other cases ...
         default:
             // Code to be executed if none of the cases match
             break;
     }

     // multiple params
     using System;

      class Program
      {
          static void Main()
          {
              Console.WriteLine("Enter two numbers separated by a space:");
              string input = Console.ReadLine();
              string[] parts = input.Split();

              if (parts.Length != 2)
              {
                  Console.WriteLine("Invalid input format. Please enter two numbers separated by a space.");
                  return;
              }

              string firstParam = parts[0];
              string secondParam = parts[1];

              // Use tuple pattern matching with switch
              switch ((firstParam, secondParam))
              {
                  case ("1", "a"):
                      Console.WriteLine("First param is '1' and second param is 'a'.");
                      break;
                  case ("2", "b"):
                      Console.WriteLine("First param is '2' and second param is 'b'.");
                      break;
                  default:
                      Console.WriteLine("No matching case found.");
                      break;
              }
          }
      }

     ```

- shorthand way

  ```csharp
      int number = 30;

    switch (number)
    {
      case 100:
        Console.WriteLine("Number is 100");
        break;
      case < 100:
        Console.WriteLine("Number is less than 100");
        break;
      default:
        Console.WriteLine("default");
        break;
    }

    string result = number switch
    {
      > 100 => "Number is greater than 100",
      < 100 => "Number is less than than 100",
      _ => "Number is 100",
    };
    Console.WriteLine(result);
  ```

- switch can also help us to check data types

  ```csharp
    object number = 30;

    switch (number)
    {
      case int:
        Console.WriteLine("input is int");
        break;
      case string:
        Console.WriteLine("input is string");
        break;
      default:
        Console.WriteLine("default");
        break;
    }
  ```

- checking the data type in switch

```csharp
 object number = 30;

    switch (number)
    {
      case int inputInt: // if you need additional manipulation with the value rename it
        inputInt++;
        Console.WriteLine("input is int");
        break;
      case string inputString:
        Console.WriteLine(inputString.Length);
        Console.WriteLine("input is string");
        break;
      default:
        Console.WriteLine("default");
        break;
    }
```

- switch and method

  ```csharp
    using System;

    class Program
    {
        static void Main()
        {
            Console.WriteLine("Calculator");

            Console.Write("Enter the first number: ");
            double num1 = GetValidNumber();

            Console.Write("Enter the second number: ");
            double num2 = GetValidNumber();

            Console.Write("Enter the operation (+, -, *, /): ");
            char operation = GetValidOperation();

            switch ((operation, num1, num2))
            {
                case ('+', var a, var b):
                    Console.WriteLine($"{a} + {b} = {a + b}");
                    break;
                case ('-', var a, var b):
                    Console.WriteLine($"{a} - {b} = {a - b}");
                    break;
                case ('*', var a, var b):
                    Console.WriteLine($"{a} * {b} = {a * b}");
                    break;
                case ('/', var a, var b) when b != 0:
                    Console.WriteLine($"{a} / {b} = {a / b}");
                    break;
                case (_, _, _) when num2 == 0:
                    Console.WriteLine("Cannot divide by zero.");
                    break;
                default:
                    Console.WriteLine("Invalid operation.");
                    break;
            }
        }

        static int GetValidNumber()
        {
          int number;
          // int.TryParse(Console.ReadLine(), out number)
          // The second parameter is an out parameter, which means it will be assigned the parsed int value if the parsing succeeds.
          while (!int.TryParse(Console.ReadLine(), out number))
          {
            Console.Write("Invalid input. Please enter a valid number: ");
          }
          return number;
        }

        static double GetValidNumber()
        {
            double number;
            while (!double.TryParse(Console.ReadLine(), out number))
            {
                Console.Write("Invalid input. Please enter a valid number: ");
            }
            return number;
        }

        static char GetValidOperation()
        {
            char operation;
            while (!char.TryParse(Console.ReadLine(), out operation) || !IsValidOperation(operation))
            {
                Console.Write("Invalid input. Please enter a valid operation (+, -, *, /): ");
            }
            return operation;
        }

        static bool IsValidOperation(char operation)
        {
            return operation == '+' || operation == '-' || operation == '*' || operation == '/';
        }
    }

  ```

#### program 1 positive, negative or zero

```csharp
   // program 1. positive, negative or zero
   using System;
   class Test
   {
   public static void Main(string[] args)
   {
      int number = 0;
      if (number > 0)
      {
         Console.WriteLine("Positive Number");
      }
      else if (number < 0)
      {
         Console.WriteLine("Negative Number");
      }
      else
      {
         Console.WriteLine("Zero");
      }
   }
   }
```

#### program 2: digit spelling program

```csharp
// program 2: digit spelling program
using System;
class Test
{
  public static void Main(string[] args)
  {
    // digit - 0-9
    // digit spelling program

    Console.Write("Enter any digit between 0 and 9: ");
    int digit = Convert.ToInt32(Console.ReadLine());

    if (digit == 0)
    {
      Console.WriteLine("Zero");
    }
    else if (digit == 1)
    {
      Console.WriteLine("One");
    }
    else if (digit == 2)
    {
      Console.WriteLine("Two");
    }
    else if (digit == 3)
    {
      Console.WriteLine("Three");
    }
    else if (digit == 4)
    {
      Console.WriteLine("Four");
    }
    else if (digit == 5)
    {
      Console.WriteLine("Five");
    }
    else if (digit == 6)
    {
      Console.WriteLine("Six");
    }
    else if (digit == 7)
    {
      Console.WriteLine("Seven");
    }
    else if (digit == 8)
    {
      Console.WriteLine("Eight");
    }
    else if (digit == 9)
    {
      Console.WriteLine("Nine");
    }
    else
    {
      Console.WriteLine("Not a valid digit.");
    }
  }
}
```

#### Assignment 7: Even/Odd numbers

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    int number;
    Console.Write("Enter a number: ");
    number = Convert.ToInt32(Console.ReadLine());

    if (number % 2 == 0)
    {
      Console.WriteLine($"{number} is Even");
    }
    else
    {
      Console.WriteLine($"{number} is Odd");
    }
  }
}


```

#### program 3: large number between 2 numbers

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    int number1, number2;

    Console.Write("number1: ");
    number1 = Convert.ToInt32(Console.ReadLine());

    Console.Write("number2: ");
    number2 = Convert.ToInt32(Console.ReadLine());

    if (number1 > number2)
    {
      Console.WriteLine($"{number1} is large number");
    }
    else if (number2 > number1)
    {
      Console.WriteLine($"{number2} is large number");
    }
    else
    {
      Console.WriteLine($"numbers are equal");
    }
  }
}


```

#### Assignment 8: Small number between 2 numbers

#### program 4: large number between 3 numbers

```csharp
using System;

class Program {
    static void Main() {
        Console.Write("Enter three numbers separated by spaces: ");
        string[] input = Console.ReadLine().Split(' ');

        int num1 = int.Parse(input[0]);
        int num2 = int.Parse(input[1]);
        int num3 = int.Parse(input[2]);

        if (num1 >= num2 && num1 >= num3) {
            Console.WriteLine($"{num1} is the largest.");
        } else if (num2 >= num1 && num2 >= num3) {
            Console.WriteLine($"{num2} is the largest.");
        } else {
            Console.WriteLine($"{num3} is the largest.");
        }
    }
}
```

#### program 5: leap year or not

```csharp
using System;

class Program {
    static void Main() {
        Console.Write("Enter a year: ");
        int year = int.Parse(Console.ReadLine());

        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
            Console.WriteLine($"{year} is a leap year.");
        } else {
            Console.WriteLine($"{year} is not a leap year.");
        }
    }
}
```

#### program 6: Capital or small letter

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    char letter;

    Console.Write("Enter any letter: ");
    letter = Convert.ToChar(Console.ReadLine());

    if (letter >= 'A' && letter <= 'Z')
    {
      Console.WriteLine($"{letter} is a capital letter");
    }
    else
    {
      Console.WriteLine($"{letter} is a small letter");
    }
  }
}

```

#### program 7: Vowel or consonant

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    char letter;

    Console.Write("Enter any letter: ");
    letter = Convert.ToChar(Console.ReadLine()); // A

    letter = char.ToLower(letter);

    if (letter == 'a' || letter == 'e' || letter == 'i' || letter == 'o' || letter == 'u')
    {
      Console.WriteLine($"{letter} is a Vowel");
    }
    else
    {
      Console.WriteLine($"{letter} is a consonant");
    }
  }
}


```

#### Assignment 9: Grade Calculator

```csharp

**Objective:** Create a simple program that calculates and displays the letter grade based on the percentage score entered by the user.

**Instructions:**

1. **Input:**
   - Prompt the user to enter their percentage score.
   - Validate the input to ensure it is a number between 0 and 100.

2. **Grade Calculation:**
   - Use if-else statements to determine the letter grade based on the following grading scale:
     - A: 90-100
     - B: 80-89
     - C: 70-79
     - D: 60-69
     - F: 0-59

3. **Output:**
   - Display the calculated letter grade to the user.

**Example Output:**
Enter your percentage score: 85
Your grade is: B


**Grading:**
- Correct calculation of letter grade: 70%
- Input validation: 20%
- Code structure, comments, and readability: 10%

**Additional Challenges:**
1. Allow the user to input their scores for multiple subjects and calculate the overall GPA.
2. Implement a switch statement instead of if-else for grade calculation.
3. Handle edge cases, such as negative scores or scores above 100, gracefully.

This assignment allows students to practice if-else statements, input validation, and basic program structure. They can also extend the functionality to make it more complex based on their skill level.
```

```csharp
// assignment solution
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter your percentage score: ");
        double percentage;

        if (double.TryParse(Console.ReadLine(), out percentage) && percentage >= 0 && percentage <= 100)
        {
            char grade;

            if (percentage >= 90)
            {
                grade = 'A';
            }
            else if (percentage >= 80)
            {
                grade = 'B';
            }
            else if (percentage >= 70)
            {
                grade = 'C';
            }
            else if (percentage >= 60)
            {
                grade = 'D';
            }
            else
            {
                grade = 'F';
            }

            Console.WriteLine($"Your grade is: {grade}");
        }
        else
        {
            Console.WriteLine("Invalid input. Please enter a valid percentage between 0 and 100.");
        }
    }
}

// solution with switch
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter your percentage score: ");
        double percentage;

        if (double.TryParse(Console.ReadLine(), out percentage) && percentage >= 0 && percentage <= 100)
        {
            char grade;

            switch ((int)percentage / 10)
            {
                case 10:
                case 9:
                    grade = 'A';
                    break;
                case 8:
                    grade = 'B';
                    break;
                case 7:
                    grade = 'C';
                    break;
                case 6:
                    grade = 'D';
                    break;
                default:
                    grade = 'F';
                    break;
            }

            Console.WriteLine($"Your grade is: {grade}");
        }
        else
        {
            Console.WriteLine("Invalid input. Please enter a valid percentage between 0 and 100.");
        }
    }
}


```

#### Program 8: switch digit spelling program

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    // switch, break, case, default

    int digit;
    Console.Write("Enter a digit: ");
    digit = Convert.ToInt32(Console.ReadLine());

    switch (digit)
    {
      case 0:
        Console.WriteLine("Zero");
        break;
      case 1:
        Console.WriteLine("One");
        break;
      case 2:
        Console.WriteLine("Two");
        break;
      case 3:
        Console.WriteLine("Three");
        break;
      case 4:
        Console.WriteLine("Four");
        break;
      case 5:
        Console.WriteLine("Five");
        break;
      case 6:
        Console.WriteLine("Six");
        break;
      case 7:
        Console.WriteLine("Seven");
        break;
      case 8:
        Console.WriteLine("Eight");
        break;
      case 9:
        Console.WriteLine("Nine");
        break;
      default:
        Console.WriteLine("Not a digit");
        break;
    }

  }
}

```

#### Program 9: switch vowel/consonant program

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    char input;
    Console.Write("Enter a single character: ");
    input = Convert.ToChar(Console.ReadLine());

    switch (Char.ToLower(input))
    {
      case 'a':
      case 'e':
      case 'i':
      case 'o':
      case 'u':
        Console.WriteLine($"{input} is a Vowel");
        break;
      default:
        if (Char.IsLetter(input))
        {
          Console.WriteLine($"{input} is a Consonant");
        }
        else
        {
          Console.WriteLine($"{input} is not a letter");
        }
        break;
    }

  }
}


```

#### Assignment 10: Weekdays/Weekend Program

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    Console.Write("Enter a day of the week : ");
    string day = Console.ReadLine();
    
    switch (day.ToLower())
    {
      case "monday":
      case "tuesday":
      case "wednesday":
      case "thursday":
      case "friday":
        Console.WriteLine("Weekday");
        break;
      case "saturday":
      case "sunday":
        Console.WriteLine("Weekend");
        break;
      default:
        Console.WriteLine("Invalid day entered");
        break;
    }

  }
}

```

#### project 1: small temperature converter project using switch

```csharp
// switch: temperature converter
using System;
class Test
{
  public static void Main(string[] args)
  {
    Console.WriteLine("Temperature Converter Started");
    Console.WriteLine("Choose 1. Fahrenheit to Celsisus");
    Console.WriteLine("Choose 2. Celsisus to Fahrenheit");

    int choice = Convert.ToInt32(Console.ReadLine());

    switch (choice)
    {
      case 1:
        Console.Write("Enter Fahrenheit temperature: ");
        double fahrenheit = Convert.ToDouble(Console.ReadLine());
        double celsisus = (fahrenheit - 32) / 1.8;
        Console.Write($"Temperature in Celsisus : {celsisus:F2} ");
        break;
      case 2:
        Console.Write("Enter Celsisus temperature: ");
        double cels = Convert.ToDouble(Console.ReadLine());
        double fahr = cels * 1.8 + 32;
        Console.Write($"Temperature in Fahrenheit : {fahr:F2} ");
        break;
      default:
        Console.WriteLine("Invalid Choice");
        break;
    }


  }
}
```

#### project 2: small calculator project using switch

```c
// switch: basic calculator
using System;
class Test
{
  public static void Main(string[] args)
  {
    int number1, number2;
    char operation;

    Console.Write("Enter an operation (+,-,*,/) : ");
    operation = Convert.ToChar(Console.ReadLine());

    Console.Write("Enter number1: ");
    number1 = Convert.ToInt32(Console.ReadLine());

    Console.Write("Enter number2: ");
    number2 = Convert.ToInt32(Console.ReadLine());

    switch (operation)
    {
      case '+':
        Console.WriteLine($"{number1} + {number2} = {number1 + number2}");
        break;
      case '-':
        Console.WriteLine($"{number1} - {number2} = {number1 - number2}");
        break;
      case '*':
        Console.WriteLine($"{number1} * {number2} = {number1 * number2}");
        break;
      case '/':
        if (number2 != 0)
        {
          Console.WriteLine($"{number1} / {number2} = {number1 / number2}");
        }
        else
        {
          Console.WriteLine("Can not divide by zero");

        }
        break;
      default:
        Console.WriteLine("Invalid operation");
        break;
    }

  }
}

```

### 3.2 Loop control statement

1. **while Loop:**
   - The `while` loop is used to repeatedly execute a block of code as long as the specified condition is true.

     ```csharp
     while (condition)
     {
         // Code to be executed while the condition is true
     }
     ```

2. **do-while Loop:**
   - The `do-while` loop is similar to the `while` loop, but it ensures that the block of code is executed at least once.

     ```csharp
     do
     {
         // Code to be executed
     } while (condition);
     ```

3. **for Loop:**
   - The `for` loop is used to repeatedly execute a block of code a specific number of times.

     ```csharp
     for (initialization; condition; update)
     {
         // Code to be executed in each iteration
     }
     ```

4. **foreach Loop:**
   - The `foreach` loop is used to iterate over elements in a collection (e.g., arrays, lists).

     ```csharp
     foreach (var item in collection)
     {
         // Code to be executed for each item in the collection
     }
     ```

     In C#, the `foreach` loop does not directly provide access to the index of the elements being iterated over. However, you can achieve this by using the `IEnumerable<T>.Select()` extension method along with the `Enumerable.Range()` method to generate indices. Here's how you can do it:

      ```csharp
      using System;
      using System.Linq;

      class Program
      {
          static void Main()
          {
              int[] numbers = { 1, 2, 3, 4, 5 };

              // Using Select with Range to get indices
              foreach (var index in Enumerable.Range(0, numbers.Length))
              {
                  Console.WriteLine($"Index: {index}, Value: {numbers[index]}");
              }
          }
      }
      ```

      In this example, `Enumerable.Range(0, numbers.Length)` generates a sequence of numbers from 0 to `numbers.Length - 1`, which represents the indices of the array. Then, we use `Select` to iterate over these indices, and within the loop, we access both the index and the corresponding element from the array.

These control statements provide flexibility and help in creating more dynamic and responsive programs in C#.

#### Program 10: print from 1 to 100

#### Program 11: series

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    Console.Write("Enter the start number: ");
    int start = Convert.ToInt32(Console.ReadLine());

    Console.Write("Enter the last number: ");
    int end = Convert.ToInt32(Console.ReadLine());

    Console.Write("Enter the difference number: ");
    int diff = Convert.ToInt32(Console.ReadLine());

    for (int count = start; count <= end; count = count + diff)
    {
      Console.Write($"{count} ");
    }

  }
}

// 1 2 3 4 ... 100
// 1 3 5 7 ... 99
// 2 4 6 8 ... 100
// 2 5 8 11 ... 

```

#### Program 12: sum of even/odd numbers

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    int sum = 0;
    for (int i = 1; i <= 10; i++)
    {
      if (i % 2 != 0)
      {
        sum = sum + i;
      }
    }
    Console.WriteLine($"Sum of odd numbers = {sum}");
  }
}
// 2+4+6+8+10=30
```

#### Program 13: Factorial

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    Console.Write("Enter a number : ");
    int number = Convert.ToInt32(Console.ReadLine());
    int fact = 1;
    for (int i = number; i >= 1; i--)
    {
      fact = fact * i;
    }
    Console.WriteLine($"Factorial({number}) = {fact}");
  }
}
// 5 = 5*4*3*2*1 = 120
// 4 = 4*3*2*1= 24
// 3 = 3*2*1 = 6
// 2 = 2*1 = 2
```

#### break and continue keyword

#### Nested loop

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    for (int i = 1; i <= 3; i++)
    {
      for (int j = 1; j <= 5; j++)
      {
        Console.WriteLine($"i={i}, j={j} : Bangladesh");
      }
    }
  }
}
// outer loop i=1 1<=3
// inner loop j=1 1<=5 Bangladesh
// inner loop j=2 2<=5 Bangladesh
// inner loop j=3 3<=5 Bangladesh
// inner loop j=4 4<=5 Bangladesh
// inner loop j=5 5<=5 Bangladesh
// inner loop j=6 6<=5 

// outer loop i=2 2<=3
// inner loop j=1 1<=5 Bangladesh
// inner loop j=2 2<=5 Bangladesh
// inner loop j=3 3<=5 Bangladesh
// inner loop j=4 4<=5 Bangladesh
// inner loop j=5 5<=5 Bangladesh
// inner loop j=6 6<=5 

// outer loop i=3 3<=3
// inner loop j=1 1<=5 Bangladesh
// inner loop j=2 2<=5 Bangladesh
// inner loop j=3 3<=5 Bangladesh
// inner loop j=4 4<=5 Bangladesh
// inner loop j=5 5<=5 Bangladesh
// inner loop j=6 6<=5 

// outer loop i=4 4<=3

```

#### project 3: Multiplication table

```csharp
using System;
class Test
{
  public static void Main(string[] args)
  {
    Console.Write("Enter start number: ");
    int startNumber = Convert.ToInt32(Console.ReadLine());

    Console.Write("Enter end number: ");
    int endNumber = Convert.ToInt32(Console.ReadLine());

    for (int i = startNumber; i <= endNumber; i++)
    {
      for (int j = 1; j <= 10; j++)
      {
        Console.WriteLine($"{i} X {j} = {i * j}");
      }
      Console.WriteLine("--------------------");
    }

  }
}

// start number = 2
// end number = 8

// number = 5
// number X i = number*i
// 5 X 1 = 5  
// 5 X 2 = 10
// ....
// 5 X 10 = 50
```

## Basic 4. Methods / function

- use capital letter for Method Name
- what to learn?
      - how to define a function
      - how to call a function
      - how to pass parameters to a function
      - how to return from a function

- Method: A method is a block of code created inside a class that performs a specific task or operation. It is a fundamental building block in any programming language and is defined within a class or a struct. Methods are used to encapsulate logic, promote code reusability, and organize code into manageable units.

```csharp
// AccessModifier ReturnType MethodName(ParameterType parameter1, ParameterType parameter2, ...)
// {
//     // Method body
//     // Code to perform the task
//     // Optionally, return a value of ReturnType
// }

public class MyClass
{
    // Example method without parameters and return type
    public void SimpleMethod()
    {
        // Method body
        Console.WriteLine("Hello from SimpleMethod!");
    }

    // Example method with parameters and return type
    public int Add(int a, int b)
    {
        // Method body
        int sum = a + b;
        return sum;
    }
}
```

### Assignment 11: create a calculator using function

Certainly! Here's a simple project idea for practicing methods in C#: a basic calculator application.

**Calculator Project:**

**Requirements:**

1. Create a C# console application.
2. Define a `Calculator` class that contains methods for basic arithmetic operations (addition, subtraction, multiplication, division).
3. Implement a menu-driven interface that allows the user to choose an operation and input operands.
4. Perform the selected operation and display the result.

**Code Example:**

```csharp
using System;

class Calculator
{
    public int Add(int a, int b)
    {
        return a + b;
    }

    public int Subtract(int a, int b)
    {
        return a - b;
    }

    public int Multiply(int a, int b)
    {
        return a * b;
    }

    public double Divide(int a, int b)
    {
        if (b != 0)
        {
            return (double)a / b;
        }
        else
        {
            Console.WriteLine("Error: Cannot divide by zero.");
            return double.NaN;
        }
    }
}

class Program
{
    static void Main()
    {
        Calculator calculator = new Calculator();

        while (true)
        {
            Console.WriteLine("Simple Calculator");
            Console.WriteLine("1. Add");
            Console.WriteLine("2. Subtract");
            Console.WriteLine("3. Multiply");
            Console.WriteLine("4. Divide");
            Console.WriteLine("5. Exit");

            Console.Write("Choose an operation (1-5): ");
            string choice = Console.ReadLine();

            if (int.TryParse(choice, out int operation) && operation >= 1 && operation <= 5)
            {
                if (operation == 5)
                {
                    Console.WriteLine("Exiting the calculator. Goodbye!");
                    break;
                }

                Console.Write("Enter the first operand: ");
                int operand1 = int.Parse(Console.ReadLine());

                Console.Write("Enter the second operand: ");
                int operand2 = int.Parse(Console.ReadLine());

                int result = 0;

                switch (operation)
                {
                    case 1:
                        result = calculator.Add(operand1, operand2);
                        break;
                    case 2:
                        result = calculator.Subtract(operand1, operand2);
                        break;
                    case 3:
                        result = calculator.Multiply(operand1, operand2);
                        break;
                    case 4:
                        double divisionResult = calculator.Divide(operand1, operand2);
                        if (!double.IsNaN(divisionResult))
                        {
                            Console.WriteLine($"Result: {divisionResult}");
                        }
                        continue; // Skip displaying the result for division until the end
                }

                Console.WriteLine($"Result: {result}");
            }
            else
            {
                Console.WriteLine("Invalid choice. Please enter a number between 1 and 5.");
            }

            Console.WriteLine();
        }
    }
}
```

This simple calculator project allows students to practice creating a class with methods to perform different operations, handle user input, and implement a menu-driven interface.

### Assignment 12: create an area calculator - triangle, rectangle

### Project 4 - Converter Project

Certainly! Here's a simple C# console application for a converter that converts between units. In this example, let's create a basic length converter:

```csharp
using System;

class Program
{
    static void Main()
    {
        while (true)
        {
            Console.WriteLine("Unit Converter");
            Console.WriteLine("1. Convert Inches to Centimeters");
            Console.WriteLine("2. Convert Centimeters to Inches");
            Console.WriteLine("3. Exit");

            Console.Write("Choose an operation (1-3): ");
            string choice = Console.ReadLine();

            if (int.TryParse(choice, out int operation) && operation >= 1 && operation <= 3)
            {
                if (operation == 3)
                {
                    Console.WriteLine("Exiting the unit converter. Goodbye!");
                    break;
                }

                switch (operation)
                {
                    case 1:
                        Console.Write("Enter length in inches: ");
                        if (double.TryParse(Console.ReadLine(), out double inches))
                        {
                            double centimeters = InchesToCentimeters(inches);
                            Console.WriteLine($"{inches} inches is equal to {centimeters} centimeters.");
                        }
                        else
                        {
                            Console.WriteLine("Invalid input for inches.");
                        }
                        break;
                    case 2:
                        Console.Write("Enter length in centimeters: ");
                        if (double.TryParse(Console.ReadLine(), out double centimeters))
                        {
                            double inches = CentimetersToInches(centimeters);
                            Console.WriteLine($"{centimeters} centimeters is equal to {inches} inches.");
                        }
                        else
                        {
                            Console.WriteLine("Invalid input for centimeters.");
                        }
                        break;
                }
            }
            else
            {
                Console.WriteLine("Invalid choice. Please enter a number between 1 and 3.");
            }

            Console.WriteLine();
        }
    }

    private static double InchesToCentimeters(double inches)
    {
        return inches * 2.54;
    }

    private static double CentimetersToInches(double centimeters)
    {
        return centimeters / 2.54;
    }
}
```

This simple converter allows users to convert lengths between inches and centimeters. Users can choose the desired conversion, enter the length, and get the converted result. Feel free to expand and modify the converter to include other units or functionalities based on your needs.

## Intermediate 1. OOP

### Classes and Objects

- class: A template from individual object is created. A class is a custom data type or blueprint. It defines the data and behavior for a type. We can have variables and methods in a class.

- object: An object is a instance of a class.

- by default all class member is private. we can use dot operator to assign value to a class member.

```csharp
class Student{
  public string name;
  public int age;
  public static DisplayInfo(){
    Console.WriteLine();
  }
}
class Test{
  public static void Main(string[] args){
    Student s1 = new Student();
    s1.name="Anisul";
  }
}

```

### OOP 1: Encapsulation

- Encapsulate -> group (members in a class) and protect (access modifiers for the class members).
- encapsulation is the idea of "surrounding" an entity, not just to keep what's inside together, but also to protect it. hiding from outside using private.
- benefits of encapsulation
  - You can control access or modification of the data.
  - You can make the code more flexible and easy to change with new requirements.
  - Change one part of code without affecting other parts of code.
- Access modifiers: public, private, protected, internal, protected internal. The public access modifier makes the member accessible from the outside of the class. The private access modifier makes members accessible only from within the class and hides them from the outside.

```csharp
class Student
{
  private string fullName;
  private int age;

  public void SetFullName(string fName)
  {
    fullName = fName;
  }

  public string GetFullName()
  {
    return fullName;
  }
  public void SetAge(int age)
  {
    this.age = age;
  }

  public int GetAge()
  {
    return age;
  }
}

class Test
{
  public static void Main(string[] args)
  {
    Student s1 = new Student();
    s1.SetFullName("Anisul Islam");
    s1.SetAge(33);
    Console.WriteLine(s1.GetFullName());
    Console.WriteLine(s1.GetAge());
  }
}
```

### Constructor

- a special public method that has no return type and called automatically when the object is created.

### Properties

- encapsulate members and give access them with Property a public member that will have accessor (get and set accessors)

```csharp
class Student
{
  private string name; // field
  public string Name // property
  {
    set { name = value; }
    get { return name; }
  }
}

class Test
{
  public static void Main(string[] args)
  {
    Student s1 = new Student();
    s1.Name = "Anisul Islam";
    Console.WriteLine(s1.Name);
  }
}

class Student
{
  private string name; // field
  public string Name // property
  {
    set;
    get;
  }
}


// shorthand if we are not doing anything with the field
class Test
{
  public static void Main(string[] args)
  {
    Student s1 = new Student();
    s1.Name = "Anisul Islam";
    Console.WriteLine(s1.Name);
  }
}
```

### Array

```csharp
// for vs foreach
class Test
{
  public static void Main(string[] args)
  {
    string[] names = new string[3];
    names[0] = "Anisul";
    names[1] = "Nusrat";
    names[2] = "Alex";

    string[] names = new string[3] { "Anisul", "Nusrat", "Alex" };

    string[] names = { "Anisul", "Nusrat", "Alex", "Sathi", "Bob" };

    for (int index = 0; index < names.Length; index++)
    {
      Console.WriteLine(names[index]);
    }

    foreach (string name in names)
    {
      Console.WriteLine(name);
    }
  }
}

class Test
{
  public static void Main(string[] args)
  {
    string[] names = { "Anisul", "Nusrat", "Alex", "Sathi", "Bob" };

    foreach (string name in names)
    {
      Console.WriteLine(name);
    }
  }
}

class Test
{
  public static void Main(string[] args)
  {
    int[] numbers = { -10, 20, -30, 40, 50 };
    int sum = 0;
    foreach (int number in numbers)
    {
      sum = sum + number;
    }
    Console.WriteLine(sum);
  }
}

class Test
{
  public static void Main(string[] args)
  {
    int[] numbers = { -10, 20, -30, 40, 50, 0 };
    foreach (int number in numbers)
    {
      if (number > 0)
      {
        Console.WriteLine(number);
      }
    }
  }
}
```

- 2D Array

A 2D array in C# is an array of arrays, meaning it's an array where each element is also an array. This creates a grid-like structure, where elements are accessed using two indices: one for the row and one for the column.

A few real-life examples of 2D arrays:

1. **Image Representation**: Images can be represented as 2D arrays of pixels. Each element of the array stores information about the color of the corresponding pixel.

2. **Game Boards**: In games like Chess, Checkers, or Tic-Tac-Toe, the game board can be represented using a 2D array. Each element of the array represents a square on the board, and the value of the element indicates the state of that square (empty, occupied by a player's piece, etc.).

3. **Spreadsheet Data**: Spreadsheets, like Excel, organize data into rows and columns. Each cell in a spreadsheet can be thought of as an element in a 2D array.

4. **Maps**: Maps in computer graphics or geographical applications are often represented using 2D arrays. Each element of the array corresponds to a location on the map, and the value of the element represents attributes such as elevation, terrain type, or population density.

5. **Matrix Operations**: Matrices in mathematics are commonly represented using 2D arrays. They are used in various applications, including computer graphics, physics simulations, and solving systems of linear equations.

6. **Seating Arrangements**: In venues like theaters, stadiums, or classrooms, seating arrangements can be represented using a 2D array. Each element represents a seat, and the value indicates whether the seat is occupied or available.

These are just a few examples of how 2D arrays are used in real-life scenarios. They are versatile data structures that find applications in many fields of computer science and beyond.

Here's how you can declare, initialize, and work with 2D arrays in C#:

**Declaration and Initialization:**

```csharp
// example 1: declare,initialize, print a simple 2D Array
public class MyClass
{
  public static void Main(string[] args)
  {
    int[,] matrix = new int[2, 3];
    matrix[0, 0] = 1;
    matrix[0, 1] = 2;
    matrix[0, 2] = 3;

    matrix[1, 0] = 4;
    matrix[1, 1] = 5;
    matrix[1, 2] = 6;

    Console.Write($"{matrix[0, 0]} ");
    Console.Write($"{matrix[0, 1]} ");
    Console.Write($"{matrix[0, 2]} ");

    Console.WriteLine();
    Console.Write($"{matrix[1, 0]} ");
    Console.Write($"{matrix[1, 1]} ");
    Console.Write($"{matrix[1, 2]} ");

    Console.ReadKey();

  }

}

// example 2: declare and initailze a simple 2D Array
public class MyClass
{
  public static void Main(string[] args)
  {
    int[,] matrix = { { 1, 2, 3 }, { 4, 5, 6 } };

    Console.Write($"{matrix[0, 0]} ");
    Console.Write($"{matrix[0, 1]} ");
    Console.Write($"{matrix[0, 2]} ");

    Console.WriteLine();
    Console.Write($"{matrix[1, 0]} ");
    Console.Write($"{matrix[1, 1]} ");
    Console.Write($"{matrix[1, 2]} ");

    Console.ReadKey();

  }

}

// example 3: Iterating Over the Array with loop
public class MyClass
{
  public static void Main(string[] args)
  {
    int[,] matrix = { { 1, 2, 3 }, { 4, 5, 6 } };

    for (int row = 0; row < matrix.GetLength(0); row++)
    {
      for (int col = 0; col < matrix.GetLength(1); col++)
      {
        Console.Write($"{matrix[row, col]} ");
      }
      Console.WriteLine();
    }
    Console.ReadKey();
  }
}


**Initializing a Jagged Array (Array of Arrays):**

Alternatively, you can use a jagged array, which is an array of arrays. It provides more flexibility as each row can have a different length.

```csharp
// 1st version:
/*
1 2
3 4 5
6 
8 9 10 11
*/
public class MyClass
{
  public static void Main(string[] args)
  {
    int[][] jaggedArray = new int[4][];

    jaggedArray[0] = new int[] { 1, 2 };
    jaggedArray[1] = new int[] { 3, 4, 5 };
    jaggedArray[2] = new int[] { 6 };
    jaggedArray[3] = new int[] { 8, 9, 10, 11 };

    for (int row = 0; row < jaggedArray.Length; row++)
    {
      for (int col = 0; col < jaggedArray[row].Length; col++)
      {
        Console.Write($"{jaggedArray[row][col]} ");
      }
      Console.WriteLine();

    }


    Console.ReadKey();
  }
}

// 2nd version: 
/*
1 2
3 4 5
6 
8 9 10 11
*/
public class MyClass
{
  public static void Main(string[] args)
  {
    int[][] jaggedArray = new int[][]
    {
      new int[] { 1, 2 },
      new int[] { 3, 4, 5 },
      new int[] { 6 },
      new int[] { 8, 9, 10, 11 }
    };

    for (int row = 0; row < jaggedArray.Length; row++)
    {
      for (int col = 0; col < jaggedArray[row].Length; col++)
      {
        Console.Write($"{jaggedArray[row][col]} ");
      }
      Console.WriteLine();

    }


    Console.ReadKey();
  }
}

// 3rd version
/*
1 2
3 4 5
6 
8 9 10 11
*/
public class MyClass
{
  public static void Main(string[] args)
  {
    int[][] jaggedArray = new int[][]
    {
      new int[] { 1, 2 },
      new int[] { 3, 4, 5 },
      new int[] { 6 },
      new int[] { 8, 9, 10, 11 }
    };

    foreach (var row in jaggedArray)
    {
      foreach (var item in row)
      {
        Console.Write($"{item} ");
      }
      Console.WriteLine();

    }


    Console.ReadKey();
  }
}

// 4th version
/*
1 2
3 4 5
6 
8 9 10 11
*/
public class MyClass
{
  public static void Main(string[] args)
  {
    int[][] jaggedArray =
    {
      new [] { 1, 2 },
      new [] { 3, 4, 5 },
      new [] { 6 },
      new [] { 8, 9, 10, 11 }
    };

    foreach (var row in jaggedArray)
    {
      foreach (var item in row)
      {
        Console.Write($"{item} ");
      }
      Console.WriteLine();

    }


    Console.ReadKey();
  }
}

// 5th version

public class MyClass
{
    public static void Main(string[] args)
    {
        int[][] jaggedArray = new int[4][];

        jaggedArray[0] = new int[] { 1 };
        jaggedArray[1] = new int[] { 2, 3 };
        jaggedArray[2] = new int[] { 4, 5, 6 };
        jaggedArray[3] = new int[] { 7, 8 };

        for (int row = 0; row < jaggedArray.Length; row++)
        {
            for (int col = 0; col < jaggedArray[row].Length; col++)
            {
                Console.Write($"{jaggedArray[row][col]} ");
            }
            Console.WriteLine();
        }
        Console.ReadKey();
    }
}
```

**Usage Considerations:**

- Use a 2D array when you need a fixed-size grid with consistent row and column counts.
- Use a jagged array when you need flexibility in row lengths or when the array elements represent different sizes of data.

- A challenage collected from Sololearn

```csharp
 class Program
    {
        static void Main(string[] args)
        {
            int day1Winner = Convert.ToInt32(Console.ReadLine());
            int day2Winner = Convert.ToInt32(Console.ReadLine());
            int day3Winner = Convert.ToInt32(Console.ReadLine());


            string[][] olympiad = new string[][]
            {
                //day 1 - 5 participants
                new string[] { "Jill Yan", "Bridgette Ramona", "Sree Sanda", "Jareth Charlene", "Carl Soner" },
                //day 2 - 7 participants
                new string[] { "Anna Hel", "Mariette Vedrana", "Fran Mayur", "Drake Hilmar", "Nikolay Brooks", "Eliana Vlatko", "Villem Mario" },
                //day 3 - 4 participants
                new string[] { "Hieremias Zavia", "Ziya Ollie", "Christoffel Casper", "Kristian Dana", }

            };
            //your code goes here                 
            Console.WriteLine(olympiad[0][day1Winner-1]);
            Console.WriteLine(olympiad[1][day2Winner-1]);
            Console.WriteLine(olympiad[2][day3Winner-1]);               
           
            
        }
    }
```

#### User Input for Array

Certainly! Here's the modified code with exception handling added:

```csharp
using System;

public class MyClass
{
    public static void Main(string[] args)
    {
        try
        {
            // Get user input for the size of the 1D array
            Console.Write("Enter the size of the 1D array: ");
            int size1D = int.Parse(Console.ReadLine());

            // Create and initialize the 1D array based on user input
            int[] array1D = new int[size1D];
            Console.WriteLine("Enter elements for the 1D array:");
            for (int i = 0; i < size1D; i++)
            {
                Console.Write($"Enter element {i + 1}: ");
                array1D[i] = int.Parse(Console.ReadLine());
            }

            // Get user input for the size of the 2D array (number of rows)
            Console.Write("\nEnter the number of rows for the 2D array: ");
            int rows = int.Parse(Console.ReadLine());

            // Create and initialize the 2D array based on user input
            int[][] array2D = new int[rows][];
            Console.WriteLine("Enter elements for the 2D array:");
            for (int i = 0; i < rows; i++)
            {
                Console.Write($"Enter the number of elements for row {i + 1}: ");
                int cols = int.Parse(Console.ReadLine());
                array2D[i] = new int[cols];
                Console.WriteLine($"Enter elements for row {i + 1}:");
                for (int j = 0; j < cols; j++)
                {
                    Console.Write($"Enter element {j + 1}: ");
                    array2D[i][j] = int.Parse(Console.ReadLine());
                }
            }

            // Display the 1D array
            Console.WriteLine("\n1D Array:");
            foreach (int num in array1D)
            {
                Console.Write(num + " ");
            }

            // Display the 2D array
            Console.WriteLine("\n\n2D Array:");
            foreach (int[] row in array2D)
            {
                foreach (int num in row)
                {
                    Console.Write(num + " ");
                }
                Console.WriteLine();
            }
        }
        catch (FormatException)
        {
            Console.WriteLine("Invalid input! Please enter a valid integer.");
        }
        catch (OverflowException)
        {
            Console.WriteLine("The input is too large or too small.");
        }
        catch (OutOfMemoryException)
        {
            Console.WriteLine("Out of memory. Unable to create arrays with such large dimensions.");
        }
        catch (Exception ex)
        {
            Console.WriteLine($"An error occurred: {ex.Message}");
        }
        finally
        {
            Console.ReadKey();
        }
    }
}
```

This code now includes exception handling for various scenarios, such as when the user enters invalid input (e.g., non-integer values), when the input is too large or too small, or when there's not enough memory to create the arrays. The `finally` block ensures that the program waits for a key press before exiting, regardless of whether an exception occurred or not.

#### Tic-Tac-Toe game

Sure, here's a basic console application in C# that uses a 2D array to represent a Tic-Tac-Toe game:

```csharp
using System;

class TicTacToe
{
    // 2D array to represent the game board
    private char[,] board;

    // Constructor to initialize the game board
    public TicTacToe()
    {
        board = new char[3, 3];
        InitializeBoard();
    }

    // Method to initialize the game board with empty cells
    private void InitializeBoard()
    {
        for (int row = 0; row < 3; row++)
        {
            for (int col = 0; col < 3; col++)
            {
                board[row, col] = '-';
            }
        }
    }

    // Method to display the current state of the game board
    private void DisplayBoard()
    {
        Console.WriteLine("  0 1 2");
        for (int row = 0; row < 3; row++)
        {
            Console.Write(row + " ");
            for (int col = 0; col < 3; col++)
            {
                Console.Write(board[row, col] + " ");
            }
            Console.WriteLine();
        }
    }

    // Method to check if a player has won
    private bool CheckWin(char player)
    {
        // Check rows and columns
        for (int i = 0; i < 3; i++)
        {
            if ((board[i, 0] == player && board[i, 1] == player && board[i, 2] == player) ||
                (board[0, i] == player && board[1, i] == player && board[2, i] == player))
            {
                return true;
            }
        }

        // Check diagonals
        if ((board[0, 0] == player && board[1, 1] == player && board[2, 2] == player) ||
            (board[0, 2] == player && board[1, 1] == player && board[2, 0] == player))
        {
            return true;
        }

        return false;
    }

    // Method to play the game
    public void PlayGame()
    {
        char currentPlayer = 'X';
        int moves = 0;

        Console.WriteLine("Welcome to Tic-Tac-Toe!");
        DisplayBoard();

        while (moves < 9)
        {
            Console.WriteLine($"Player {currentPlayer}'s turn");
            Console.Write("Enter row and column (e.g., '0 1'): ");
            string[] input = Console.ReadLine().Split(' ');
            int row = int.Parse(input[0]);
            int col = int.Parse(input[1]);

            if (row < 0 || row >= 3 || col < 0 || col >= 3 || board[row, col] != '-')
            {
                Console.WriteLine("Invalid move. Try again.");
                continue;
            }

            board[row, col] = currentPlayer;
            DisplayBoard();

            if (CheckWin(currentPlayer))
            {
                Console.WriteLine($"Player {currentPlayer} wins!");
                return;
            }

            currentPlayer = (currentPlayer == 'X') ? 'O' : 'X';
            moves++;
        }

        Console.WriteLine("It's a draw!");
    }
}

class Program
{
    static void Main(string[] args)
    {
        TicTacToe game = new TicTacToe();
        game.PlayGame();
    }
}
```

This code creates a basic Tic-Tac-Toe game where two players (X and O) take turns placing their marks on a 3x3 grid. The game checks for wins and draws after each move and displays the current state of the board.


### OOP 2: Inheritance

### Exception Handling

```csharp
  Console.Write("Enter a number: ");
    int num = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine(num);
```

Exception handling in C# allows you to manage runtime errors gracefully by catching and handling exceptional conditions that might occur during program execution. This prevents your program from crashing and provides a mechanism to respond to errors in a controlled manner. Here's an overview of exception handling in C#:

1. **Try-Catch Block**: The basic structure for handling exceptions is the `try-catch` block. Code that might raise an exception is enclosed within the `try` block, and any potential exceptions are caught and handled in the `catch` block.

   ```csharp
   try
   {
       // Code that might throw an exception
   }
   catch (ExceptionType ex)
   {
       // Handle the exception
       // ex.Message
   }
   ```

2. **Exception Types**: You can catch specific types of exceptions by specifying the exception type in the `catch` block. This allows you to handle different types of exceptions differently.

   ```csharp
   try
   {
       // Code that might throw an exception
   }
   catch (DivideByZeroException ex)
   {
       // Handle divide by zero exception
   }
   catch (ArgumentException ex)
   {
       // Handle argument exception
   }
   catch (Exception ex) // Catch-all for other exceptions
   {
       // Handle other exceptions
   }
   ```

3. **Finally Block**: You can optionally include a `finally` block after the `catch` block. Code in the `finally` block is executed whether an exception occurs or not. This block is commonly used for cleanup tasks such as closing resources.

   ```csharp
   try
   {
       // Code that might throw an exception
   }
   catch (Exception ex)
   {
       // Handle the exception
   }
   finally
   {
       // Cleanup code
   }
   ```

4. **Throwing Exceptions**: You can explicitly throw exceptions using the `throw` keyword. This is useful for indicating errors or exceptional conditions within your code.

   ```csharp
   if (condition)
   {
       throw new Exception("An error occurred.");
   }
   ```

5. **Custom Exceptions**: You can define your own exception types by creating classes that derive from `Exception`. This allows you to create custom exception types tailored to your application's needs.

   ```csharp
   public class CustomException : Exception
   {
       public CustomException(string message) : base(message)
       {
       }
   }
   ```

6. **Exception Handling Best Practices**:
   - Catch specific exceptions rather than using a generic `catch (Exception ex)` block.
   - Provide meaningful error messages or log information when handling exceptions.
   - Use exception handling judiciously and avoid catching exceptions that you cannot handle properly.

Exception handling is a fundamental aspect of robust software development in C#, helping you write more reliable and resilient applications.

## Intermediate 2. aaa

## .NET 

