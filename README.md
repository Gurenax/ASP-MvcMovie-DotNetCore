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

5. Change `Welcome()` method to
```csharp
// GET: /HelloWorld/Welcome/ 
// Requires using System.Text.Encodings.Web;
public string Welcome(string name, int numTimes = 1)
{
    return HtmlEncoder.Default.Encode($"Hello {name}, NumTimes is: {numTimes}");
}
```

6. Change `Welcome()` method to
```csharp
public string Welcome(string name, int ID = 1)
{
    return HtmlEncoder.Default.Encode($"Hello {name}, ID: {ID}");
}
```

## Reference
https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app-xplat/start-mvc