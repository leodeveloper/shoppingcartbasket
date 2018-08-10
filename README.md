# Shopping cart basket
Shopping cart basket web application, web api, web api client application, Asp.net core, asp.net core web api, entityframwork core in memory

This is prototype web api, web application and client application.

The solution consist following projects

Ecommerce.WebApi (Asp.net web api core)

Ecommerce.Web (Asp.net web application core)

Ecommerce.WebApi.Client (C# client liberary core)

Ecommerce.Model (C# Model Layer)

Ecommerce.Service (C# service Layer)

Ecommerce.Test (Xunit Test project)


# Ecommerce.WebApi (Asp.net web api core)

Settings

Ecommerce.WebApi Under Properties there is file called launchsettings.json

 Default Url    "launchUrl": "api/product/",
 
 Enviroment     "environmentVariables": {"ASPNETCORE_ENVIRONMENT": "Development"},
 
 Api Url        "applicationUrl": "http://localhost:61493"
 
 
Ecommerce.WebApi the is file called startup.cs

Database Settings

Under Configuration method, For in memory storage using Microsoft.EntityFrameworkCore.InMemory 


EF Core database providers do not have to be relational databases. InMemory is designed to be a general purpose database for testing, and is not designed to mimic a relational database.

# services.AddDbContext<EnityFramWorkDbContext>(opt => opt.UseInMemoryDatabase("TestDb"));
      
Switch from in memory database to actuall database by change the single line of code.

In startup.cs these is a method calls AddTestData, this method is populate the data into Product table and BasketItem table

The default route for api is http://localhost:61492/api/product/

you can change the default route in startup.cs

# Swegger
Swagger is also configure in this web api project, the url for swagger is http://localhost:61492/swagger

