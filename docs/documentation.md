# Documentation
All documentation in a codebase should be in Moonwave format, which is readable and able to be auto-compiled to a generated documenation website.

Moonwave for generating doc websites is a separate tool, which you can find here: https://eryn.io/moonwave/. This page covers the documentation format, not the page generator.

Documentation should be written in Moonwave format for the following:
* High-level modules (ones that are used across the game, not a random sub-module)
* Open-sourced modules
* Modules that are critical for functionality

When writing Moonwave comments, use comment blocks by starting with `--[=[` and ending with `]=]`. For example:

```lua
--[=[
    This is a class written in Moonwave format

    @class ClassName
]=]
```

Also when writing Moonwave comments, opt to always use `@param`, `@class`, and `@return` tags when applicable, and make sure to describe parameters and return data. Anything else is optional but nice to have. When writing a description for a function, make sure to include a Luau snippet. For example:

```lua
--[=[
    Thing that does thing.

    ```lua
    Module:DoThing(5)
    ``

    @param Foo number -- The parameter that does thing
]=]

function Module:DoThing(Foo : number)
    --...
end
```

Also, be sure to sprinkle normal comments made with `--` around your code, especially in parts that are hard to understand without further context. If a developer wouldn't be able to understand something, put a comment on it. Put a space before and after typing a comment declaration.