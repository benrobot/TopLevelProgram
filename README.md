## Requirements
To attempt to build these solutions you must have both version 5.x and 6.x of the DotNet SDKs. Each folder has a `global.json` to ensure the correct SDK is used when attempting to build.

## Problem
The top-level program in the repo fails to build sometimes with the following error:
```
Error CS0246 The type or namespace name 'Program' could not be found (are you missing a using directive or an assembly reference?)
```

[![Dotnet5Ubuntu](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet5-ubuntu.yml/badge.svg)](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet5-ubuntu.yml)

[![Dotnet5Windows](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet5-windows.yml/badge.svg)](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet5-windows.yml)

[![Dotnet6Ubuntu](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet6-ubuntu.yml/badge.svg)](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet6-ubuntu.yml)

[![Dotnet6Windows](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet6-windows.yml/badge.svg)](https://github.com/benrobot/TopLevelProgram/actions/workflows/dotnet6-windows.yml)

## Weirdness
This repository was created to show case a build for a top-level program failing in .NET 5 when it references it's own class `Program` within the code.

## Additional Weirdness
|                             | DotNet5 | DotNet6 |
|-----------------------------|---------|---------|
| `dotnet build`              | fails   | builds  |
| Visual Studio 2019 16.11.10 | fails   | fails   |
| Visual Studio 2022 17.1.0   | builds  | builds  |
