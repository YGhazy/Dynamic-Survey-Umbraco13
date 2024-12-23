
## Creation init script
```
Ensure we have the version specific Umbraco templates
dotnet new install Umbraco.Templates::13.4.0 --force

# Create solution/project
dotnet new sln --name "UmbracoInit"
dotnet new umbraco --force -n "UmbracoInit" --friendly-name "Administrator" --email "admin@example.com" --password "1234567890" --connection-string "Server=(localdb)\\MSSQLLocalDB;Database=UmbracoInitDB;Integrated Security=true;" --connection-string-provider-name "Microsoft.Data.SqlClient"
dotnet sln add "UmbracoInit"

#Add starter kit
dotnet add "UmbracoInit" package clean --version 4.1.0

dotnet run --project "UmbracoInit"
#Running
```
