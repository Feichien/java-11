# Java 11

## Java SE 11 Programmer I

### Understanding Java Technology and environment

### Creating a Simple Java Program

### Working With Java Primitive Data Types and String APIs

1. Java is a statically typed language. This means that the data type of a variable is defined at compile time and cannot change during run time. 
1. Java has primitive and reference variables. The Java compiler and JVM inherently know what primitive types mean, while reference data types are built by combining primitive data types and other reference data types.
1. Primitive data types below:

    | Date Type | Size    | Description                                                             | Sample                  |
    |-----------|---------|-------------------------------------------------------------------------|-------------------------|
    | byte      | 1 byte  | -128 to 127                                                             | -1, 0, 1                |
    | short     | 2 bytes | -32,768 to 32,767                                                       | 0, 1, 2, 'a', '\u00061' |
    | int       | 4 bytes | -2,147,483,648 to 2,147,483,647                                         | -1, 2, 3                |
    | long      | 8 bytes | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807                 | -1, 2, 3                |
    | float     | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits | -1, 2, 3                |
    | double    | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits     | 1.1f, 2.0f              |
    | boolean   | 1 bit   | Stores true or false values                                             | 1.1, 2.0                |
    | char      | 2 bytes | Stores a single character                                               | true, false             |

    Wrapper classes exist for Byte, Short, Integer, Long, Float and Double.

1. Reference types include:
    * Classes
    * Interfaces
    * Enums
    
1. A variable contains a raw number, and assigning one variable to another simply copies that number from one variable to another. Java uses **pass by value** semantics.
1. Java initialises all static and instance variables of a class automatically if you don't initialise them explicitly. You must initalise local variables explicitly before they are used.
1. Assigning a smaller type to a larger type is known as **implicit widening conversion** as no cast is required. To assign a larger type to a smaller type, for a compile time constant (i.e. final) the compiler will automatically narrow the value. If the source variable is not a constant then a cast is required, this is known as **explicit narrowing**. Determining the value that will actually be assigned when doing an explicit can be complicated.

### Using Operators and Decision Constructs

1. Arithmetic operators are used to perform standard mathematical operations on all primitive variables (and wrapper objects for numeric types) except boolean.
1. Operators and their precedence shown below:

    | Operator Type | Category             | Precadence                              |
    |---------------|----------------------|-----------------------------------------|
    | Unary         | postfix              | expr++ expr--                           |
    | Unary         | prefix               | ++expr --expr +expr -expr ~ !           |
    | Arithmetic    | multiplicative       | * / %                                   |
    | Arithmetic    | additive             | + -                                     |
    | Shift         | shift                | << >> >>>                               |
    | Relational    | comparison           | < > <= >= instanceof                    |
    | Relational    | equality             | == !=                                   |
    | Bitwise       | bitwise AND          | &                                       |
    | Bitwise       | bitwise exclusive OR | ^                                       |
    | Bitwise       | bitwise inclusive OR | \|                                      |
    | Logical       | logical AND          | &&                                      |
    | Logical       | logical OR           | \|\|                                    |
    | Ternary       | ternary              | ? :                                     |
    | Assignment    | assignment           | = += -= *= /= %= &= ^= \|= <<= >>= >>>= |

1. Java applies the rules of **numeric promotion** while working with operators that deal with numeric values. **Unary numeric promotion** occurs if an operand is smaller than int, the operand is automatically promoted to int. **Binary numeric promotion** occurs if one of the promoted operands is larger than int, and causes both operands to be promoted to the larger operand.

1. In the case of a Dangling Else statement, the Else is associated to the nearest if statement.

1. In a switch statement the expression must be:
    * Integral types (byte, char, short, int) and their wrapper classes. Note that this excludes long.
    * enum type.
    * A String.

1. In a switch statement case labels are optional, but if provided they must be compile time constants.

1. In a switch statement the default block is optional, but if provided there can only be 1.

### Working with Java Arrays

1. Examples for array instantiation:
    ```java
    int[] ia = new int[10];
    int[] ia = {0, 1, 2, 3, 4, 5};
    int[][] iaa = new int[2][3];
    int[][] iaa = new int[3][];
    int[][] iaa = new int[][]{new int[]{1,2}};
    int[][] iaa = {{1,2}};
    ``` 

1. Members of an array object include:
    * length
    * clone

1. Arrays have two interesting runtime properties:
    * They are reified meaning that type checking is done at runtime by the JVM and not the compiler.
    * They are covariant meaning that a subclass object can be stored in  an array that is declared to be the type of its superclass (i.e. you can store an integer in a number array).

1. The compare method compares 2 int arrays and returns 0 if they are equal, a value less than 0 if the first array is lexicographically less than the second array, and a value greater than 0 if the first array is lexicographically greather than the second array.

1. The mismatch method takes two int arrays and returns the index of the first mismatch, otherwise it returns -1 if no mismatch is found.

### Describing and Using Objects and Classes

### Creating and Using Methods

### Applying Encapsulation

### Reusing Implementations Through Inheritance

### Programming Abstractly Through Interfaces

### Handling Exception

### Understanding Modules

## Java SE 11 Programmer II
