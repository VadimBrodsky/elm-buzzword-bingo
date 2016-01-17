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
-- They bind a value to a name
title =
  "hello"
    |> String.toUpper
    
-- Functions are defined with the = sign
-- They can't have zero arguments
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

-- Qualified import:
import String

-- To use the String functions import the String module
-- The string functions can be used as a qualified import, qualifying the function name with the module where it is defined

String.toUpper

-- Specific module functions can be imported to the current namespace

-- Unqualified import

import String exposing (toUpper, repeat, trimRight)

-- then these function can be called in the current scope as if they were defined in the current namespace

-- to import all of the function of a module to a namespace (..)
import Html exposing (..)

-- Lists
-- Comma separated values of the same type
[1, 2, 3]

-- Elm Html module use 2 lists: attributes and nested DOM elements
h1 [ id "header", class "classy" ] [ text "Heading" ]

```
