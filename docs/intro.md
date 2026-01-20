---
sidebar_position: 1
---

# Intro
These conventions cover the following topics:
* Juxtaposition
* Capitalization
* Indentation & whitespace
* Documentation and comments
* Variable naming
* Function naming
* Userdata declaration
* Assertion and logging
* Function structure
* Table structure and access
* Architecture
* Typechecking
* OOP format

Anything that isn't listed on these docs does not have a specific convention for it. If you feel something is missing, please make an issue on the GitHub repository.

Keep code to reasonable minimum. Do not obfuscate or keep statements on single lines. Do not overwrite code. Do not repeat yourself. Do not cache inline functions, such as those from the math or cframe libraries, for example; Luau includes inline caching. Assign variables to the smallest possible scope. Return in a function as soon as possible.