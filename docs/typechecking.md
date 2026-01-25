# Typechecking
Typecheck a reasonable amount; nobody should guess if "Value" is a number, string, or table. Overtyping is still annoying.

Bad example:

```lua
for _, value in Array do
    --...
end
```

Good example:

```lua
for _, value : number in Array do
    --...
end
```

:::info

Typechecking, by these conventions, is done mostly for autofill purposes. Make sure that you can autofill everything.

That beind said, it's also helpful to attach types to arguments and more, especially if the declaration of it didn't already have the type attached.

:::

Types should be exported from modules when they represent data that is usable from outside the module.

Additionally, making modules exclusively for storing types is recommended when creating complex libraries or systems.