# Sequences

A sequence is a logical series of elements of one type where individual elements are computed ONLY as required. 
In situations where not all the elements of a collection are needed, an F# sequence performs better than an F# list.

Any type that implements *System.IEnumerable* interface can be used as a sequence. 
An F# sequence is considered as an *IEnumerable\<T\>* type in C#, therefore it is not required to add *Microsoft.FSharp.Core.dll*
