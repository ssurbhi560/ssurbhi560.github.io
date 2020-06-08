---
layout: post
title: "Types of programming languages!!"
date: 2020-6-8
---
There is no boundation on to the number of ways we can classify programming languages. Here I will be trying to focus on one of those classification related to the way of declaration of the constructs in it.
Let's first start with discussing about **statically typed language** and **dynamically typed language** first.

Before diving in to understand these, first we need know what exactly is type checking?

**Type-Checking**: It is being done by a type checker when you compile or run code written in any programming language. This verifies that the type of a constuct (constant, variable, array, list, object) matches what is expected in its usage context or not. *Type* here means whether the variable is a *char*, or an *int*, or a *double*, or a custom struct, or a pointers of aforementioned types.
Type Checking is also of two types according  to the type of programming language:
**Static Type Checking** (Type checking at compile-time) and **Dyanmic Type Checking**(Type checking at run-time)

**What is a Statically Typed language?**

Static typed programming languages are those in which there is a need to explicitely declare the type of the variable before using them and thus determined at comiple time.Once a variable is assigned to a particular data type, it can not be assigned to any other variable of different type and doing so will raise a type error at compile-time. *Static type checking* occurs during the course of compilation rather than during run time. This particular thing makes programs written in these languages run much faster as the compiled code executes more quickly because when the compiler knows the exact data types that are in use, it can produce optimized machine code (faster and/or using less memory)

**How memory is used in statically typed languages?**

When we declare a variable in these languages, an area of memory is set aside for containing values allowed by the data type of the variable. The memory allocated is interpreted as the data type is assigned. So, if it is an integer variable the memory allocated will read as an interger only. When we intialize the variable with some value, that value gets stored at the memory location. At the time of compilation, that value is being checked, if it is not same as the declared data type program will not compile and will throw a TypeError. 

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

In dynamically typed languages there is no declaration of variable, and just have an assignment statement.Variables are bound to objects at run time by means of assignment statements, and unlike statically typed languages, it is possible to bind the same variable to objects of different types during execution of the program. Here *dynamic type checking* occurs when code is run. 

**How memory is used dyanamically typed languages?**

Here the memory allocated for the variable does not know about the type of the variable until the code is run. It stores the value at some random memory location and then binds the variable to that memory container, making the value of that container accessible through that variable name. So declartion the data type does not matter here as it will get to know the type of the value at run time.

Consider the following example:

```
#Python Code
num = 10  #directly using the variable
num = "ten"  #No error caused

```

Common examples of dynamically typed language includes Python, Ruby, Dart, Lisp, R and PHP

