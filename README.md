F# is a functional-first programming language that supports multiple paradigms. It is multi-paradigm programming language that supports

* funcional programming
* imperative programming &
* object-oriented programming

### Executing F# interactively using F# Interactive (FSI)

F# Interactive is great to quickly try F# code snippets, although not a good choice for building executable binaries. 

In Visual Studio, FSI window can be accessed from the View menu

View -> Other Windows -> F# Interactive (Ctrl + Alt + F)

(or)

View -> F# Interactive (Ctrl + Alt + F)

depending on the active development profile.

**FSI Directives**



**Limitations of FSI Window**

The FSI Window does not provide the Microsoft IntelliSense support. 

### F# Script

F# scripts are an alternative to FSI to quickly tryout scripts but with the support of Microsoft IntelliSense. F# scripts are the best way to quickly tryout F# code augmented with the support of Microsoft IntelliSense without having to create an F# project.

File -> New -> File

Select F# Script File / F# Source File

### Creating an F# project

Visual Studio offers the following F# templates

![](_misc/Creating%20an%20F%23%20project.PNG)

*Console Application*: is a template for an F# console application project

*Library*: is a template for an F# class library

*Portable Library*: is a class library for F# libraries which can be executed on various Microsoft platforms (as stated in the options)

*Silverlight Library*: is a template for a Silverlight class library

*Tutorial*: is a console application that contains F# samples
