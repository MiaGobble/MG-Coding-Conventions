# Assertion and Logging
Throughout your code, make sure to properly assert and print when needed.

## String Concatenation
When concatenating a string, including for output, make sure to build strings with "`". For example:

```lua
local MyNumber = 5
local MyString = `Number = {MyNumber}`
```

## Printing
Reserve printing for the following situations:
* Debugging
* Critical state change
* Critical action

## Warning
A warning should always act similar to an error, but of course without breaking the code. Warnings are great for when you have a point of return or default in something. When warning, if it's not already there, make sure to provide a traceback so that the developer can find the issue.

```lua
warn(`My warning! {debug.traceback()}`)
```

## Error
Errors are served only for unreturnable states of failure. In other worsd, if you've reached a point where you cannot allow the script to function no matter what, throw an error. It's better to have custom errors than ones thrown by Roblox.

Errors can also be used for assertion, such as types or values in function parameters.