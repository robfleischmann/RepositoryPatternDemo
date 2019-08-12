# RepositoryPatternDemo
A demo of my preferred layout for the repository pattern

I wanted to find a organization for the repository pattern that would read easy for other developers to understand, as using this pattern is very powerful and leads to better coding practices.

Thanks to Ladislav Mrnka from stackoverflow, here is the format I prefer:

Solution
  -- Common
       - Shared features used accross all layers
       - You can also place interfaces for repositories and uow here
  -- Entities - shared among DataAccess, Business (and UI in small projects)
       - T4 template + partial classes + custom enums  
       - partial classes can contain methods with domain logic => domain objects 
  -- DataAccess - all EF dependent code here
       - EDMX or code first mapping
       - Repositories
       - UnitOfWork
  -- Business - not every project needs this assembly
       - Business services 
       - Logic like workflows
       - DTOs exposed to UI
  -- UI
       - Controllers
       - Views
       - ViewModels

Source thread: https://stackoverflow.com/a/5283973/4429355
