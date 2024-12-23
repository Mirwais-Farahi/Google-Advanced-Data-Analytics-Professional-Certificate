# Get Started with Python
### What You'll Learn

- Explain how Python is used by data professionals.
- Explore basic Python building blocks, including syntax and semantics.
- Understand loops, control statements, and string manipulation.
- Use data structures to store and organize data.

## Background
### Adrian's Background

- Adrian transitioned from nursing to a Customer Engineer role at Google Cloud, showcasing the possibility of career changes.
- He emphasizes the importance of transferable skills like critical thinking, problem-solving, and interpersonal skills in data analytics.

### Importance of Critical Thinking, Problem-Solving and Assessment

- Within advanced data analytics, critical thinking and problem solving becomes key
when trying to debug. Furthermore, when looking for answers online, you need to be able to assess what information
you're being given and understand how to apply it to fix your problem. 

## Introduction to Python
### Programming Languages: From Hardware to High-Level

- Programming languages provide instructions to computers, which ultimately rely on the binary system (ones and zeros) represented by the on/off states of transistors.
- Low-level languages, the earliest forms, were hardware-specific and complex, while high-level languages like Python use human-readable syntax, making them easier to learn and use.

### Python: A Powerful and Approachable Language

- Python's versatility, ease of learning, and extensive libraries make it a favorite among data professionals, scientists, and web developers.
- Libraries are pre-written code collections that simplify complex tasks, such as building a neural network, saving developers time and effort.

## Python and Other Languages

- Python is favored for its readability and ease of use, often drawing comparisons to spoken language, which makes it relatively simpler to learn.
- While Python excels in data analysis, many data professionals utilize multiple programming languages, each offering unique advantages and disadvantages for specific tasks.

### Factors to Consider When Comparing Programming Languages

- When comparing programming languages, it's essential to consider aspects like the speed at which they execute code, how easy they are for beginners to learn, how they manage variables, their suitability for data science tasks, and the programming paradigms they employ.
- Python, for instance, is celebrated for its focus on machine learning and automated analysis, while R is often preferred for exploratory data analysis and building comprehensive statistical libraries.

## Object Oriented Programming (OOPS)
### Understanding Objects

- Object-oriented programming revolves around "objects" which neatly package data and the code that manipulates it.
- Think of objects like building blocks. Lists, functions, and strings you've already encountered are all examples of objects in Python.

### Classes and Methods

- Every object in Python belongs to a "class," which defines its properties and behaviors.
- "Methods" are actions you can perform on objects. For example, you can use methods to modify strings, like changing their capitalization.

### The Purpose of Object-Oriented Programming

- The main purpose of object-oriented programming is to organize code into reusable and manageable components.
- It achieves this by bundling data and the functions that operate on that data into objects.
- This approach makes code easier to understand, maintain, and scale, especially for larger projects.

### More About Object-Oriented Programming

Note: This reading contains only a brief introduction to object-oriented programming. A more detailed discussion about the nuances of object-oriented programming is beyond the scope of this course.

Previously, we identified object-oriented programming as a programming paradigm that is based around objects, which can contain both data and code that manipulates that data. You may recall that a class is an object’s data type that bundles data and functionality together, and you’ve encountered some examples of this class-specific functionality in the form of methods and attributes. In this reading, you’re going to learn more about object-oriented programming and how it works. Although this certificate program will not require you to define your own classes, having a basic understanding of how this process works will be very helpful when you encounter these concepts along your learning journey.

### Review: Attributes and Methods

Python classes are powerful and convenient because they come with built-in features that simplify common data analysis tasks. These features are known as attributes and methods.

- **Attribute**: A value associated with an object or class which is referenced by name using dot notation.
- **Method**: A function that belongs to a class and typically performs an action or operation.

A simpler way of thinking about the distinction between attributes and methods is to remember that attributes are characteristics of the object, while methods are actions or operations.

For example, if the class were `Spaceship`, then attributes might be:

- `name`
- `kind`
- `speed`
- `tractor_beam`

These attributes could be accessed by typing:
'''
Spaceship.name
Spaceship.kind
Spaceship.speed
Spaceship.tractor_beam
'''
Notice that these characteristics are accessed using only a dot.

On the other hand, methods of the Spaceship class might be:

    warp()
    tractor()

These methods could be used by typing:
Spaceship.warp()
Spaceship.tractor()

- Notice that methods are followed by parentheses, and it’s possible for them to take arguments. For example, Spaceship.warp(7) could change the speed of the ship to warp seven.

#### Defining Classes with Unique Attributes and Methods

Python lets you define your own classes, each with their own special attributes and methods. This helps all different kinds of programmers to build reusable code that makes their work more efficient. You can even build the Spaceship class mentioned previously. The example, here, demonstrates how to do this.

Note: The following code block is not interactive.
'''
class Spaceship:
    def __init__(self, name, kind):
        self.name = name
        self.kind = kind
        self.speed = 0
        self.tractor_beam = False

    def warp(self, speed):
        self.speed = speed

    def tractor(self):
        self.tractor_beam = not self.tractor_beam
'''
### Key Takeaways

- Classes comprise the core objects of Python, which is why Python is known as an object-oriented language. Class objects are powerful because they contain unique tools designed specifically for that class packaged within them.
- Methods are functions that belong to a class; they perform actions or operations, and they use parentheses.
- Attributes are values or characteristics associated with a class or class instance; they do not use parentheses.
- While there are many classes, attributes, and methods pre-built into Python, there is a high level of customization offered in the object-oriented programming paradigm.

## Data Types and Coversion in Python
### Data Types in Python

- Python uses **strings** to represent text, enclosed in single or double quotes. **Integers** represent whole numbers, while **floats** represent numbers with decimals.
- Mixing data types in operations, like adding a string to an integer, can cause errors in Python.

### Converting Data Types

- **Implicit conversion** happens automatically in Python, like when an integer is converted to a float during an arithmetic operation.
- **Explicit conversion** requires you to use predefined functions like `int()`, `float()`, and `str()` to manually change a value's data type.

### Questions
1. What is an immutable data type in Python?
An immutable data type is a type of data that cannot be changed after it is created. For example, in Python, a string is an immutable data type. Once you create a string, you cannot alter its individual characters. You would need to create a new string with the desired changes. 

## Module 2: Core Building Blocks (likely title)

Functions:
Reusable blocks of code that perform specific tasks Defined with 
        def function_name(parameters):
Example:

        def greet(name):
          print("Hello, " + name + "!")
        greet("User") 

Conditional Statements:

Control the flow of code execution based on conditions Use if, elif, and else keywords.
Example:

    x = 10
    if x > 15:
      print("x is greater than 15")
    elif x == 10:
      print("x is equal to 10")
    else:
      print("x is less than 10")

Operators:

Comparison Operators: Compare values (e.g., ==, !=, >, <, >=, <=). Logical Operators: Combine conditions (e.g., and, or, not).
Example:

    age = 25
    is_student = True
    if age >= 18 and is_student:
      print("Eligible for student 

### Glossary Terms from Module 2

#### Terms and Definitions from Course 2, Module 2

- **Algorithm**: A set of instructions for solving a problem or accomplishing a task
- **Boolean**: A data type that has only two possible values, usually true or false
- **Branching**: The ability of a program to alter its execution sequence
- **Comparator**: An operator that compares two values and produces Boolean values (True/False)
- **def**: A keyword that defines a function at the start of the function block
- **Docstring**: A string at the beginning of a function’s body that summarizes the function’s behavior and explains its arguments and return values
- **elif**: A reserved keyword that executes subsequent conditions when the previous conditions are not true
- **else**: A reserved keyword that executes when preceding conditions evaluate as False
- **Function**: A body of reusable code for performing specific processes or tasks
- **if**: A reserved keyword that sets up a condition in Python
- **Logical operator**: An operator that connects multiple statements together and performs complex comparisons
- **Modularity**: The ability to write code in separate components that work together and that can be reused for other programs
- **Modulo**: An operator that returns the remainder when one number is divided by another
- **Refactoring**: The process of restructuring code while maintaining its original functionality
- **return**: A reserved keyword in Python that makes a function produce new results which are saved for later use
- **Reusability**: The capability to define code once and use it many times without having to rewrite it
- **Self-documenting code**: Code written in a way that is readable and makes its purpose clear

#### Terms and Definitions from the Previous Module

- **Argument**: Information given to a function in its parentheses
- **Assignment**: The process of storing a value in a variable
- **Attribute**: A value associated with an object or class which is referenced by name using dot notation
- **Cells**: The modular code input and output fields into which Jupyter Notebooks are partitioned
- **Class**: An object’s data type that bundles data and functionality together
- **Computer programming**: The process of giving instructions to a computer to perform an action or set of actions
- **Data type**: An attribute that describes a piece of data based on its values, its programming language, or the operations it can perform
- **Dot notation**: How to access the methods and attributes that belong to an instance of a class
- **Dynamic typing**: Variables that can point to objects of any data type
- **Explicit conversion**: The process of converting a data type of an object to a required data type
- **Expression**: A combination of numbers, symbols, or other variables that produce a result when evaluated
- **Float**: A data type that represents numbers that contain decimals
- **Immutable data type**: A data type in which the values can never be altered or updated
- **Implicit conversion**: The process Python uses to automatically convert one data type to another without user involvement
- **Integer**: A data type used to represent whole numbers without fractions
- **Jupyter Notebook**: An open-source web application for creating and sharing documents containing live code, mathematical formulas, visualizations, and text
- **Keyword**: A special word in a programming language that is reserved for a specific purpose and that can only be used for that purpose
- **Markdown**: A markup language that lets the user write formatted text in a coding environment or plain-text editor
- **Method**: A function that belongs to a class and typically performs an action or operation
- **Naming conventions**: Consistent guidelines that describe the content, creation date, and version of a file in its name
- **Naming restrictions**: Rules built into the syntax of the language itself that must be followed
- **Object**: An instance of a class; a fundamental building block of Python
- **Object-oriented programming**: A programming system that is based around objects which can contain both data and code that manipulates that data
- **Programming languages**: The words and symbols used to write instructions for computers to follow
- **String**: A sequence of characters and punctuation that contains textual information
- **Syntax**: The structure of code words, symbols, placement, and punctuation
- **Variable**: A named container which stores values in a reserved location in the computer’s memory

