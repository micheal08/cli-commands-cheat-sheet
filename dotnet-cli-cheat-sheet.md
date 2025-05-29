# .NET CLI Commands Cheat Sheet

## Project Management

- **Create new console app**  
  `dotnet new console -n MyApp`

- **Create new web app (ASP.NET Core)**  
  `dotnet new webapp -n MyWebApp`

- **Create new class library**  
  `dotnet new classlib -n MyLibrary`

- **List all available templates**  
  `dotnet new --list`

## Solution Management

- **Create new solution**  
  `dotnet new sln -n MySolution`

- **Add project to solution**  
  `dotnet sln MySolution.sln add MyApp/MyApp.csproj`

## Project Dependencies

- **Add NuGet package**  
  `dotnet add package <PackageName>`

- **List project dependencies**  
  `dotnet list package`

- **Restore packages**  
  `dotnet restore`

## Build & Run

- **Build the project**  
  `dotnet build`

- **Run the project**  
  `dotnet run`

## Publishing

- **Publish app for release**  
  `dotnet publish -c Release -o ./publish`

## Testing

- **Create test project**  
  `dotnet new xunit -n MyTests`

- **Run tests**  
  `dotnet test`

## Useful Info

- **Display info about installed SDKs**  
  `dotnet --info`

- **List installed SDKs**  
  `dotnet --list-sdks`

- **List installed runtimes**  
  `dotnet --list-runtimes`

## Help

- **General help**  
  `dotnet --help`

- **Command-specific help**  
  `dotnet <command> --help`

---
**Tip**: Replace `MyApp`, `MyWebApp`, `MyLibrary`, `MySolution`, and `<PackageName>` with your actual names.
