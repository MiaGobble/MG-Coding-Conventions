# Capitalization
Capitalization refers to the way userdata names is capitalized.

There are four main types of capitalization:
* *Pascal case* (`PascalCase`), which makes every word start with a capital letter
* *Camel case* (`camelCase`), which makes every word start with a capital letter, except the first word
* *Upper case* (`UPPER_CASE`), which makes every letter capitalized, with words separated by underscores
* *Snake case* (`snakecase`), which makes every letter lowercase

In the MG Coding Conventions, *pascal case* is the default for every userdata except the declared exceptions below. *Snake case* is never used. The reason it's best to opt for *pascal case* is because a majority of the Roblox API uses that casing, and so having userdata to match a similar style is easier to read.

## Constants
Constants, which are variables that are declared once at the top of the script and never change, are always *upper case*. In this case, only do this casing if the variable is in the root part of the script towards the top, not if it's in another function.

```lua
local MY_CONSTANT = 10 -- Constant
local MyVariable = 10 -- Not constant

MyVariable = 20
```

## OOP class-wide functions
When programming in OOP format, all OOP methods (e.g. `object:Destroy()`) are named in *pascal case*. However, OOP class functions, such as constructors (e.g. `object.new()`), are always done in *camel case*.

```lua
function object.new(...) -- Class-wide function
    return --...
end

function object:Method() -- Object method
    --...
end
```

## Configuration
Configuration refers to tables or other userdata that act like constants shared across a project. Indexes in these config files are still in *pascal case*.

## Keys and actions
A key or action would refer to something like a string sent to a function that changes behavior. In a case like this, all keys are still *pascal case*.