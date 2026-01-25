---
sidebar_position: 1
---

# Intro
These conventions cover a number of topics, such as for juxtaposition, capitalization, and more.

Anything that isn't listed on these docs does not have a specific convention for it. If you feel something is missing, please make an issue on the GitHub repository.

## Additional notes
Consider the following in addition to the rest of the conventions, as general advice:
* Keep code to reasonable minimum.
* Do not obfuscate or keep statements on single lines.
* Do not overwrite code.
* Do not repeat yourself.
* Do not cache inline functions, such as those from the math or cframe libraries, for example. Luau includes inline caching.
* Assign variables to the smallest possible scope.
* Return in a function as soon as possible.