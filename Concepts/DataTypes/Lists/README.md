# Lists

A List collection type in F# has the following properties:

* a collection of elements of identical type
* an ordered collection of elements
* support indexing (i.e. random access of its elements)
* immutable
* is a linked list
* supports structural equality, which allows to check for list equivalence (i.e. two lists are equal if they both have same elements); lists can be compared only if their elements support equality comparisons
* only congruent lists can be compared; trying to compare incongruent lists results in a compilation error

### List literal

```fsharp
[1; 2; 3; 4; 5]
```

Unlike C#, the elements of a list in F# are separted by a ';'

### Defining a List

**Creating an empty list**

```fsharp
Microsoft (R) F# Interactive version 14.0.23413.0
Copyright (c) Microsoft Corporation. All Rights Reserved.

For help type #help;;

> let emptyList = [];;

val emptyList : 'a list

> let emptyListA = List.empty;;

val emptyListA : 'a list
```

**Using a list literal to create a List**

A List can be created using a list literal

```fsharp
Microsoft (R) F# Interactive version 14.0.23413.0
Copyright (c) Microsoft Corporation. All Rights Reserved.

For help type #help;;

> let listA = [1; 2; 3; 4; 5];;

val listA : int list = [1; 2; 3; 4; 5]

> let listB = [1..10];;

val listB : int list = [1; 2; 3; 4; 5; 6; 7; 8; 9; 10]

> let listC = [for iter = 1 to 10 do yield iter * 2];;

val listC : int list = [2; 4; 6; 8; 10; 12; 14; 16; 18; 20]
```

### Accessing elements

Elements of a list can be accessed by using an indexer, which unlike in C#, has to be used with a '.' notation. 
The list name has to be succeeded with a '.' operator followed by the indexer. 

```fsharp
> let listA = [1; 2; 3; 4; 5];;

val listA : int list = [1; 2; 3; 4; 5]

> listA.[2];;
val it : int = 3
```

### List operators

**cons operator (::)**

The :: operator adds an element to a list at its head. It works by invoking the constructor of the F#'s list class that accepts an element and a list and returns a new list with the element added at the front of the list.

```fsharp
Microsoft (R) F# Interactive version 14.0.23413.0
Copyright (c) Microsoft Corporation. All Rights Reserved.

For help type #help;;

> let listA = [2; 3; 4; 5];;

val listA : int list = [2; 3; 4; 5]

> let listB = 1::listA;;

val listB : int list = [1; 2; 3; 4; 5]
```

**concatenation operator (@)**

The '@' operator concatenates two lists and returns a new list.

Time complexity is O(min(N1, N2)) where N1 is size of list A and N2 is size of list B

```fsharp
Microsoft (R) F# Interactive version 14.0.23413.0
Copyright (c) Microsoft Corporation. All Rights Reserved.

For help type #help;;

> let listA = [1; 2; 3];;

val listA : int list = [1; 2; 3]

> let listB = [4; 5; 6];;

val listB : int list = [4; 5; 6]

> let listC = listA @ listB;;

val listC : int list = [1; 2; 3; 4; 5; 6]
```
