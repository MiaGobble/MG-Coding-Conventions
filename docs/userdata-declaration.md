# Userdata Declaration
Always use the `local` keyword within any scope, including the top one. Functions have function syntax, variables have variable syntax.

When defining functions, put `function` before the name, not after.

```lua
foo = 5 -- Bad

local foo = 5 -- Good

function bar() -- Bad

end

local bar = function() -- Bad

end

local function bar() -- Good

end
```