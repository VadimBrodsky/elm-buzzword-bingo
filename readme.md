# ELM

```elm
-- a single line comment

{-
a multi
line
comment
-}

-- each file is a module, Hello.elm
module Hello where

--- other modules can to be imported
import String

-- an Elm program starts with a main function
main =

-- Calling functions
String.toUpper 'hello'

-- Each function has set input and output types
String.toUpper  -- <function: toUpper> : String -> String

-- Return type is the last in the sequence
String.repeat   -- <function: repeat> : Int -> String -> String


-- Functions can be nested
String.reverse (String.toUpper (String.repeat 3 "lol "))

-- Or using the pipe operator, for easier reading
"lol " |> String.repeat 3 |> String.toUpper |> String.reverse
  
-- Or on multiple lines
"lol "
  |> String.repeat 3
  |> String.toUpper
  |> String.reverse

{-
- Functions in Elm are not methods, they don't run in the context of an object 
- There is not shared state, no self or this, 
- Functions can only access its argument or the values in the enclosing scope, 
- All values in Elm are immutable, Elm functions are stateless and pure
-}

-- Definitions are functions that take no arguments
title =
  "hello"
    |> String.toUpper
    
-- Functions are defined with the = sign
-- <function name> <argument> =
--   <function body>
-- The value of the last expression becomes the return value

-- Define a simple function
triple number =
  number * 3
  
-- Call it
triple 4  --> 12
  
-- Function with 2 arguments
title message times =
  message
    |> String.toUpper
    |> String.repeat times

-- Call it as any other function
title "hello" 2

-- Concatenating strings with ++
"hello" ++ " " ++ "world"

```
