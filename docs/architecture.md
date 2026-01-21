# Architecture
Everything works best when using a multi-script architecture. This means there is no centralized framework, and instead code is just modularized and loaded normally. Multiple scripts are allowed on the client and server (just don't be excessive), but they must be in their respective structure folders.

All script, asset, config, and other file names are in *pacal case* (`PascalCase`) capitalization

## File Structure
Here is the recommended file structure:
* `ReplicatedFirst`
    * `./Client`
    * `./ClientModules`
* `ServerScriptService`
    * `./Server`
    * `./ServerModules`
* `ReplicatedStorage`
    * `./Common`
        * `./Packages`
    * `./SharedAssets`
    * `./Remotes`
* `ServerStorage`
    * `./ServerAssets`

Code that is specifically for the client will go under `Client` (for scripts) or `ClientModules` (for modules). Code that is only for the server will go under `Server` (for scripts) or `ServerModules` (for modules). Anything that is shared code will go in `Common`. `Packages` are for modules imported by a package manager, such as Wally.

`SharedAssets` is for any asset that can be used by either the client or server. `ServerAssets` is for assets that are server-only. Do not ever put instances inside of code.

`Remotes` is a folder of remote events/functions for the game. They do not go anywhere else.

## Modularization
Modularization is important to make sure that functionality is divided into isolated scopes, either through functions or modules.

Functions should be reserved for splitting functionality that is part of a larger picture in a script or module. For example, a weapon might have functions to shoot, reload, etc.

Modules are used to separate bigger things to create libraries, databases, and systems. Some examples of things that are their own modules include:
* Configurations
* Utilities
* Systems
* Frameworks
* Classes
* Etc

Variable modularization is the smallest level of splitting up information into something more digestible. This is something you should eyeball, with the general rule of thumb being "if it's readable, it's good”. Make sure to utilize variables for repeated information.