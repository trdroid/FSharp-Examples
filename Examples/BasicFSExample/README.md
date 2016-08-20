### Creating a project

Create a new F# project from the "Console Application" template

![](_misc/Creating%20a%20basic%20fs%20project.PNG)

**Default Project structure and contents**

![](_misc/Basic%20FS%20project%20structure.PNG)

**Program.fs**

```fsharp
// Learn more about F# at http://fsharp.org
// See the 'F# Tutorial' project for more help.

[<EntryPoint>]
let main argv = 
    printfn "%A" argv
    0 // return an integer exit code
```
