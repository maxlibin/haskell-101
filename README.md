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
