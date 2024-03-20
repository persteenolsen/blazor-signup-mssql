# blazor-webassembly-signup-mssql

ASP.NET Core Blazor WebAssembly - User Registration and Login Example & Tutorial

# Create a global json

dotnet new globaljson --sdk-version 6.0.320 --force

# Functionality of the Web App

- JWT Authentication 
- CRUD Functionality

# Tech used for creating the Web App

- A Blazor Webassembly Client towards a .NET 6 Web API
- C#
- Razor Pages
- SQLite for the local DB - At The Server Side
- MS SQL for the remote DB - At The Server Side 
- A traditional Webhotel for hosting
- VS Code

# Development

dotnet run

# Production

Create a self contained build for production at the remote server / traditionel web hotel

dotnet publish blazorapp.csproj --configuration Release --runtime win-x86 --self-contained

Upload the build to remote server

At my remote servers the web.config needs to be without the folowing:

hostingModel="inprocess"

# Some issues to handle

_imports.razor seems not to take of the loading of the Razor files

To solve that issue I have been loading the folders / files needed like in "app.razor":

@using BlazorApp.Shared
@using Microsoft.AspNetCore.Components.Routing
@using BlazorApp.Helpers

Added the below in Blazorapp.csproj

RootNameSpace - BlazorApp - RootNameSpace




