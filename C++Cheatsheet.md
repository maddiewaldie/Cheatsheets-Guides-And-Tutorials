# C++ Cheat Sheet: The Basics

## Table of Contents

1. [Comments](#Comments)
2. [Operators](#Operators)
3. [Variables](#Variables)
4. [Statements](#Statements)
5. [Preprocessor Directives](#Preprocessor-Directives)
6. [Classes](#Classes)
7. [Functions](#Functions)
<!-- 8. [Namespaces I Commonly Use](#Namespaces-I-Commonly-Use) -->

## Comments

> The following snippet shows the different ways you can write comments in C++.

```cpp
// Single Line Comment

/*
    Multi
    Line
    Comment
*/
```

## Operators

> The following snippet shows the different arithmetic, assignment, comparison, and logical operators used in C++.

```cpp
+ // Addition

- // Subtraction

* // Multiplication

/ // Division

% // Modulus

++ // Increment (by 1)

-- // Decrement (by 1)

== // Equal to

!= // Not equal to

< // Less than

> // Greater than

>= // Greater than or equal to

<= // Less than or equal to

&& // Logical and

|| // Logical or

! // Logical not
```

## Variables

> The following snippet shows the different data types in C++, as well as how to initialize and set variables.

```cpp
/* Initializing Variables */

bool isThisFun; // Boolean - true or false

int numberOfBugsInCode; // Integer - whole number

float daysInYear;// Float

double pi;// Double - number with decimal points

char firstLetter;// Char - a single character

/* Setting Variables */

isThisFun = true;

numberOfBugsInCode = 0;

daysInYear = 365.25;

pi = 3.141592653589;

firstLetter = a;
```

## Statements

> The following snippet gives examples of common logical statements.

```cpp
/* If / Else if / Else Statement */

if (x == y) {
    z = 1;
}
else if (w == x) {
    z = 2;
}
else {
    z = 3
}

/* While Loop */

while (i < 100) {
  cout << i << "\n";
  i++;
}

/* For Loop */

for (int i = 0; i < 100; i++) {
  cout << i << "\n";
}

/* Switch Statement */

switch (day) {
  case 1:
    cout << "Monday";
    break;
  case 2:
    cout << "Tuesday";
    break;
  case 3:
    cout << "Wednesday";
    break;
  case 4:
    cout << "Thursday";
    break;
  case 5:
    cout << "Friday";
    break;
  case 6:
    cout << "Saturday";
    break;
  case 7:
    cout << "Sunday";
    break;
}
```

## Preprocessor Directives

> The following snippet shows different preprocessor directives that can be used in C++. These are lines included in a program that begin with the character #, which make them different from a typical source code text. They are invoked by the compiler to process some programs before compilation.

```cpp
/* Source file inclusion */

#include <iostream> // Ways for including a standard or user-defined file in the program
#include "class.h"

/* Constants */

#define VAR 0 // Constant value
#define X = 1

/* Ifdef Statement */

#ifdef VAR == 1
  int i = 1;
#elif X == 1
  int i = 1;
#else
  int i = 0;
#endif
```

## Classes & Functions

> The following snippet shows how to create a class in C++.

``` cpp
/* Class Definition (header file) */

class ClassName
{
    public: // Public members are accessible from anywhere where the object is visible
        Constructor(int parameter);
        virtual ~Deconstructor();

        void Function1();
        bool Function2(double var1);

    protected: // Protected members are accessible from other members of the same class, and also from members of their derived classes.
      bool isSomethingTrue;

    private: // Private members of a class are accessible only from within other members of the same class
      int number1;
      double number2;

}

/* Class Example (src file) */
class ClassName::ClassName(int parameter) { // Constructor example
  number1 = 1;
  number2 = parameter;
  isSomethingTrue = false;
}

class ClassName::~ClassName() { // Decoonstructor example
  delete number1;
  delete parameter;
}

void ClassName::Function1() { // Function example
  isSomethingTrue = true;
}

bool ClassName::Function2(double var1) {
  if (var1 == number1) {
    return true;
  }
  return false;
}
```
<!-- 
## Namespaces I Commonly Use

``` cpp



``` -->
