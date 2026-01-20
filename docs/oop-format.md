# OOP Format
Follow this format for writing OOP code:

```lua
local Object = {}
Object.__index = Object

function Object.new(Foo : number, Bar : string)
    local self = setmetatable({}, Object) -- UNSEALED TABLE!!!

    self.Foo = Foo
    self.Bar = Bar

    self:Init()

    return self
end

function Object:Init()
    -- Initialization
    self:Method()
end

function Object:Method()
    -- ...
end

return Object
```

Things to note:
* OOP is done best with metatables
* `__index` is declared at the top, right alongside the class declaration
* `.new` makes a variable of the top of that scope called `self`, which is an unsealed metatable
* Using `.new` calls `:Init()` before returning `self`