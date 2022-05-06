## Haskell 101

### Resources: https://www.youtube.com/watch?v=cTN1Qar4HSw

### What is haskell

Haskell is a strong statically typed, purely functional, lazily evaludated, general purpose.

### What is purely functional?

Everything is a function, everything is immutable, everything is an expression, no side effects.

\*\*Side effects are in IO

### What does it mean lazily evaludated

Deffered expression evaluation

Not used and is not computed

Cons:

- Memory pitfall
- IO and Parallelism pitfall

Pro:

- Huge optimizations
- Great exoressivity

### Reading of function types

```
f::Int->Int->[Int]
```

functions are auto curried, each fn only takes one argument carry to next fn and takes only another one argument and so on until it returns something.

Example: `map:: (a -> b) -> [a] -> [b]`
you can write like
Haskell can create your own operator:

```
($) :: (a -> b) -> a -> b
```

This operator takes create a function, takes in ````a and return b

this is the same as creating a function for example

```
let example = fun (x + y)
```

you can write like

```
let example = fun $ x + y
```

another popular operator which is dot (.)

```
(.):: (b -> c) -> (a -> b) -> (a -> c)
```

Type alias:

```
type Point = (Int, Int) -- tuple

type Point = [Point] -- list

type Map k v = [(k v)] --type parameter
```

User `data` to create a new dataType and use `type` to alias a type

You can also declare struct inside a dataType

```
data User = User { userName:: String, userAge:: Int }
```

How to write functions in haskell, first give a type of the function then function: example

```
not:: Bool -> Bool -- Declare a function of not signature where takes in a Bool and returns a Bool
not True = False
not False = True -- Use pattern matching for simplify the expression
```

In pattern matching you can use `_` as whatever this is, pattern matching can be use for deconstruction

Some good place to start haskell:

tryhaskell.org
learnhaskell.com
book.realworldhaskell.org
haskellbook.com
haskell.org/hoogle/

List in Haskell is represent by (x:xs), it can be [] which is empty list if (x:xs) which means list with head and list of xs
