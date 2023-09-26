# CMPG-323-Project-2---25431285-

**project2ecopowersolutions.azurewebsites.net**

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

###### Authentical Folder
An Authentical folder was created, with all related files pertaining to the Authentication folder. The following classes were in the Authentication folder are: ApplicationUser.cs(which contains properties for UserName PasswordHash, email), ApplicationDbContext.cs(providing all necessary database sets properties nedded to manage the identity tables in the SQL Server), UserRoles.cs(needs to identify the respective roles types - either admin or user), RegisterModel.cs(requires the user to register using the user name, email, and password), LoginModel.cs(once user has registred, then they can login using the username and password), Response.cs(gives a response in terms of a message, stating the status) with code added to the respective classes

###### Controllers folder
AuthenticationController handles the authentication and registration endpoints for the users.
The constructor injects instances of UserManager, RoleManager, and IConfiguration services. These services are used to manage user data, roles, and configuration.
Login Endpoint takes a LoginModel object as a parameter, which contains the user's username and password. If the provided credentials are valid, it generates a JWT token containing the user's claims and returns it.

###### Program.cs
The program.cs has been updated with the provided code.

###### WeatherForecast
The Authorize attribute is applied to restrict access to authenticated users, which is applied at the controller level.

###### Migration

###### Reference List
REFERENCE LIST

•	10 aug CMPG323 Weekly Virtual class API controllers (2023) YouTube. Available at: https://youtu.be/kiSJGGy29fY?si=sXsXzKiaah0Kf5LO (Accessed: 16 August 2023). 
•	ASP net core rest api get by Id (2020) YouTube. Available at: https://youtu.be/6ilQiWRV7Qs?si=QEewgnq7AcqBXADE (Accessed: 20 August 2023). 
•	ASP.NET Core - scaffolding with Entity Framework Core (database first approach) (2020) YouTube. Available at: https://youtu.be/SnU4Ulee_NI?si=bRPKPT9LE_JXqd1I (Accessed: 20 August 2023). 
•	Azure ad password protection: Setup and configuration (2019) YouTube. Available at: https://youtu.be/sYqj3QMX31M?si=1EX5vYW4_oUVpFA_ (Accessed: 20 August 2023). 
•	Create ASP.NET core web application using visual studio 2022 (2021) YouTube. Available at: https://youtu.be/dTIjAJO-tcQ?si=PpIt1eYAlc1SfH-d (Accessed: 20 August 2023). 
•	Deploy API on azure (2021) YouTube. Available at: https://youtu.be/_ickMK1kMIA?si=L6xEBW92kiSyu90R (Accessed: 20 August 2023). 
•	Deploy the database to azure SQL (no date) Sitefinity CMS Deploy and upgrade. Available at: https://www.progress.com/documentation/sitefinity-cms/deploy-the-database-to-azure-sql (Accessed: 20 August 2023). 
•	Implementing DELETE METHOD IN ASP net web api (2016) YouTube. Available at: https://youtu.be/LTFv362D0mI?si=IZLDj4pNKCyO7qdv (Accessed: 22 August 2023). 
•	Implementing post method in ASP net web api (2016) YouTube. Available at: https://youtu.be/0eGUix3Nkjg?si=mBwM5E6zGQ6ToBoq (Accessed: 22 August 2023). 
•	Rajendran, P. (2023) Azure API app vs web app - comparison, Serverless360. Available at: https://www.serverless360.com/blog/azure-api-app-vs-web-app (Accessed: 23 August 2023). 
•	Rick-Anderson (no date) Retrieving and displaying data with model binding and web forms, Microsoft Learn. Available at: https://learn.microsoft.com/en-us/aspnet/web-forms/overview/presenting-and-managing-data/model-binding/retrieving-data (Accessed: 21 August 2023). 
•	Set up Microsoft azure SQL server and SQL database (STEP-by-step tutorial) (2023) YouTube. Available at: https://youtu.be/6joGkZMVX4o?si=qTZ9dW3TCMxyEkJ_ (Accessed: 21 August 2023). 
•	Update data with HTTP PUT REQUEST: Angular HTTP: Angular 13+ (2022) YouTube. Available at: https://youtu.be/ASFZsGJ5ZuE?si=H367Ooq8ki3oroOP (Accessed: 25 August 2023). 
•	Author: Jacqui MullerFeel free to reach out or browse through:LinkedInGitHubThe JPanda – Automation et al. blogs et al. (2022) Join two entities in .NET core, using Lambda and entity Framework Core, JD Bots. Available at: https://jd-bots.com/2022/01/24/join-two-entities-in-net-core-using-lambda-and-entity-framework-core/ (Accessed: 18 August 2023). 
•	Haddad, R. (2023) Git branching strategies: Gitflow, Github Flow, trunk based..., AB Tasty. Available at: https://www.abtasty.com/blog/git-branching-strategies/ (Accessed: 31 August 2023). 
•	API World. (2023). API Integration Best Practices. Retrieved from https://apiworld.co/integration-best-practices/. Accessed on August 30, 2023.
•	
•	    Smith, T. (2023). Cloud-Native Application Development with .NET Core. Cloud Tech Journal, 14(2), 55-68.
•	
•	    Docker. (n.d.). Docker Compose. Retrieved from https://docs.docker.com/compose/. Accessed on August 29, 2023.
•	
•	    Microsoft Docs. (n.d.). Azure Resource Groups. Retrieved from https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal. Accessed on August 28, 2023.
•	
•	    GitHub Blog. (2023). GitHub Actions: Continuous Integration and Continuous Deployment. Retrieved from https://github.blog/changelog/2023-02-03-github-actions-virtual-environments-for-ci-cd/. Accessed on August 27, 2023.
•	
•	    Microsoft Learn. (n.d.). Microsoft Certified: Azure Solutions Architect Expert. Retrieved from https://learn.microsoft.com/en-us/certifications/azure-solutions-architect. Accessed on August 26, 2023.
•	
•	    Agile Alliance. (n.d.). Scrum vs. Kanban: Comparing Agile Project Management Frameworks. Retrieved from https://www.agilealliance.org/agile101/agile-glossary/#q=~(infinite~false~filters~(postType~(~'Agile%20Glossary))~searchTerm~'scrum%20vs%20kanban~sort~false~sortDirection~'asc~page~1). Accessed on August 25, 2023.
•	
•	    Microsoft Azure. (n.d.). Azure Functions. Retrieved from https://azure.microsoft.com/en-us/services/functions/. Accessed on August 24, 2023.
•	
•	    TechCrunch. (2023). API Economy: Driving Business Growth. Retrieved from https://techcrunch.com/api-economy-business-growth. Accessed on August 23, 2023.
•	
•	    Martin, L. (2023). DevOps Practices: Continuous Integration and Continuous Deployment. DevOps Today, 8(1), 22-35.
•	
•	    Microsoft Docs. (n.d.). .NET Core CLI Overview. Retrieved from https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet. Accessed on August 22, 2023.
•	
•	    API World. (2023). Securing Your API: Best Practices. Retrieved from https://apiworld.co/securing-your-api-best-practices/. Accessed on August 21, 2023.
•	
•	    Smith, A. (2023). RESTful API Design Patterns. API Design Journal, 19(3), 43-57.
•	
•	    Docker. (n.d.). Docker Images. Retrieved from https://docs.docker.com/glossary/glossary/#image. Accessed on August 20, 2023.





















































