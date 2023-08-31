# CMPG-323-Project-2---25431285-
## Project 2 - Training
Prior training required for this repository is Cloud Basics and API Bacis.
The training attained for this project was: Microsoft Learning Training Badges
Describe Cloud Service Types
Describe Azure Identity Access Security
Dotnet Microservices

### Azure
Created an Azure subscription for students, with 100$ student credits, which will be used throughout the semester. After that a resource group(rgCmpg323Project2) was created, and budgets were made to ensure credits are allocated accordingly.
A SQL Database(CMPG323-Project2), SQL Server(zaarcmpg323proj2) as well as an App service(ProjectEcoPowerSolutions) were created. A query was launched under the database to create tables, with the provided cloud database script. Ther server needed us to use login details, with a created password. The database has a connection string that will be used through out the project to ensure that the project is completed.

#### ASP.NET Core Web API
Created a new project on Visual Studio, the chose the ASP.NET Core Web API. The framework used is .NET 6.0(Long-term support). Entity Framework(s) were installed by going to the Tools tab, then NuGet Package Manager, the Manage NuGet Packages for Solutions, and manually added the following Frameworks: Microsoft.EntityFrameworkCore, Microsoft.EntityFrameworkCore.SqlServer, Microsoft.EntityFrameworkCore.Design, Microsoft.EntityFrameworkCore.Tools. The chosen installation version are 6.0.21. A similar process of selecting the Tools tab, only now the Package Manager Console is clicked, where a command line appeared and "dotnet ef" was typed.

##### Scaffolding 
Scaffolding the database involves generating an Entity Framework model derived from a pre-existing database. The outcome encompasses the formation of entities, which are subsequently associated and linked to the corresponding tables within the designated database. On the command line, this line "dotnet ef dbcontext scaffold "<>"" is run with the <> being replaced by the coonection string found on azure under the SQL database. Under Models, the tables appear as cs classes. The appsettings.json file was updated with the correct format of the connection string.

##### Authentical Folder
An Authentical folder was created, with all related files pertaining to the Authentication folder. The following classes were in the Authentication folder are: ApplicationUser.cs(which contains properties for UserName PasswordHash, email), ApplicationDbContext.cs(providing all necessary database sets properties nedded to manage the identity tables in the SQL Server), UserRoles.cs(needs to identify the respective roles types - either admin or user), RegisterModel.cs(requires the user to register using the user name, email, and password), LoginModel.cs(once user has registred, then they can login using the username and password), Response.cs(gives a response in terms of a message, stating the status) with code added to the respective classes

###### Controllers folder
AuthenticationController handles the authentication and registration endpoints for the users.
The constructor injects instances of UserManager, RoleManager, and IConfiguration services. These services are used to manage user data, roles, and configuration.
Login Endpoint takes a LoginModel object as a parameter, which contains the user's username and password. If the provided credentials are valid, it generates a JWT token containing the user's claims and returns it.

####### Program.cs
The program.cs has been updated with the provided code.

######## WeatherForecast
The Authorize attribute is applied to restrict access to authenticated users, which is applied at the controller level.

######### Migration




















































