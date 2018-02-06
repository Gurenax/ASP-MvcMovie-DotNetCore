# ASP MVC Structure using .NET Core

## Steps Taken
1. Create MvcMovie app directory
```
mkdir MvcMovie
cd MvcMovie
dotnet new mvc
```

2. Press `Debug (F5)` to build and run the program.

3. App is started at `localhost:5000`

4. Create new controller `HelloWorldController.cs`
```csharp
using Microsoft.AspNetCore.Mvc;
using System.Text.Encodings.Web;

namespace MvcMovie.Controllers
{
    public class HelloWorldController : Controller
    {
        // 
        // GET: /HelloWorld/

        public string Index()
        {
            return "This is my default action...";
        }

        // 
        // GET: /HelloWorld/Welcome/ 

        public string Welcome()
        {
            return "This is the Welcome action method...";
        }
    }
}
```

## Reference
https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app-xplat/start-mvc