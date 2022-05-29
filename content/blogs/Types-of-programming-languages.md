---
title: "Types of Programming languages"
date: 2020-06-08
type: "post"
---
There is no limit to the number of ways we can classify programming languages. Here, I will be trying to focus on one particular classification which is related to the way of declaration of the constructs in the language.

Let’s start with discussing **statically typed language** and **dynamically typed language**.

Before diving in to understand these, first we need know *what is type checking?* So, let's read about that first.

**Type-Checking** is being done by a type checker when you compile or run code written in any programming language. This verifies that the type of a construct (constant, variable, array, list, object) matches what is expected in its usage context or not. Type here means whether the variable is a char, or an int, or a double, or a custom struct, or a pointer of aforementioned types. Type Checking is also of two types: **Static Type Checking** (Type checking at compile-time) and **Dynamic Type Checking** (Type checking at run-time)

**What is a Statically Typed language?**

Statically typed programming languages are those in which there is a need to explicitly declare the type of the variable before using them and thus determined at compile time. Once a variable is assigned to a particular data type, it can not be assigned to any other variable of a different type, and doing so will raise a type error at compile-time. *Static type checking* occurs during compilation rather than during run time. This particular thing makes programs written in these languages run much faster as the compiled code executes more quickly because when the compiler knows the exact data types that are in use, it can produce optimized machine code (faster and/or using less memory)

**How memory is used in statically typed languages?**

When we declare a variable in these languages, an area of memory is set aside for containing values allowed by the data type of the variable. The memory allocated is interpreted as the data type is assigned. So, if it is an integer variable the memory allocated will read as an integer only. When we initialize the variable with some value, that value gets stored at the memory location. At the time of compilation, that value is being checked, if it is not the same as the declared data type program will not compile and will throw a TypeError.

Consider the following example:

```
/* C code */

static int num, sum; //explicit declaration
num = 5; //now use the variables
sum = 10;
sum = sum + num;
```

Common examples of statically-typed languages include Java, FORTRAN, C/C++, C#, Haskell, Scala, Rust, Go and Perl.

**What is a Dynamically typed language?**

In dynamically typed languages there is no declaration of variable and just have an assignment statement. Variables are bound to objects at run time using assignment statements, and unlike statically typed languages, it is possible to bind the same variable to objects of different types during the execution of the program. Here *dynamic type checking* occurs when code is run.

**How memory is used dynamically typed languages?**

Here the memory allocated for the variable does not know about the type of the variable until the code is run. It stores the value at some random memory location and then binds the variable to that memory container, making the value of that container accessible through that variable name. So the declaration of the data type does not matter here as it will get to know the type of the value at run time.

Consider the following example:

```
/* Python Code */

num = 10  //directly using the variable
num = "ten"  //No error caused

```

Common examples of dynamically typed language includes Python, Ruby, Dart, Lisp, R and PHP