# ppserver-linux [![Build status](https://ci.appveyor.com/api/projects/status/fhxvgvt0rmhbj1qf/branch/master?svg=true)](https://ci.appveyor.com/project/mihaly044/ppserver-linux/branch/master)
A NET core port of PPServer for ParkPlaces that runs on linux

## What is PPServer?
PPServer is part of the [ParkPlaces](https://github.com/mihaly044/parkplaces/) project. It was built to serve requests for the client and to manage the database. PPServer was originally built to run on Windows, but thanks to the .NET core ppserver-linux also runs on linux systems.

**ppserver-linux** was built to run the server application for ParkPlaces in such environments where Windows is not available.

## Submodules
The original Windows PPServer uses the [WatsonTcp library](https://github.com/jchristn/WatsonTcp) by [jchristn](https://github.com/jchristn) but unfortunately it is not available for .NET core. To overcome this issue, we have created [watsontcp-dotnetcore](https://github.com/mihaly044/watsontcp-dotnetcore), a A .NET core port of WatsonTcp.

## Compiling the sources
```bash
git clone --recursive https://github.com/mihaly044/ppserver-linux.git
cd ppserver-linux
dotnet publish -c Release --runtime linux-x64 src/
```
Find the built binary in /bin/netcoreapp2.1/linux-x64/publish

## Usage & setting up
For detailed information about setting up the server, please refer to ParkPlaces' [readme](https://github.com/mihaly044/parkplaces/blob/master/README.md).
