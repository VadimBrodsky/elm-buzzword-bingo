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

-- Functions can be nested
String.reverse (String.toUpper (String.repeat 3 "lol "))

-- Or using the pipe operator, for easier reading
"lol " |> String.repeat 3 |> String.toUpper |> String.reverse
  
-- Or on multiple lines
"lol "
  |> String.repeat 3
  |> String.toUpper
  |> String.reverse


```
