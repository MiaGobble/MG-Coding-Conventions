# Tables
See [capitalization](./capitalization.md) and [userdata naming](./userdata-naming.md) for more info on this topic.

## Sealed vs Unsealed Tables
Sealed tables are reserved for constants such as configurations or settings.

Modules, classes, etc are all to be declared and mutated in an unsealed table.

## Writing and Reading Tables
Use plain `key` syntax for writing dictionaries when possible, but if there are any entries that cannot follow that, then use `["key"]` syntax. 

Use dot (table.value) notation for accessing values in a dictionary table when possible (as opposed to something like table["value"]).