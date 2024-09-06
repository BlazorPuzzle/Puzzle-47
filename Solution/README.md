# Blazor Puzzle #47

## Production Challenge

YouTube Video: https://youtu.be/RphhOCtBgmE

Blazor Puzzle Home Page: https://blazorpuzzle.com

### The Challenge:

This is a .NET 8 Global Server Blazor Web App

We are reading a value from appsettings.json and displaying it above

What do we do if we want a different message in production than in Visual Studio?

The big picture: Configuration settings can be different in production.

### The Solution:

There are multiple solutions to this problem.

The main idea with IConfiguration is that there are many layers.

Here are the ideas we mentioned:

1. **JSON file Naming Conventions**
   1. Name any .json file with the convention x.development.json or x.production.json
      1. ex: appsettings.development.json takes precedence over appsettings.json when developing in Visual Studio
      2. ex: favorites.development.json, favorites.production.json
2. **User Secrets**
   1. Right-click on the project and select **Manage User Secrets**
3. **Local Environment Variables**
   1. In Visual Studio, go to **Debug**, **[Project Name] Debug Properties**, and set **Environment Variables**
4. **Azure Environment Variables**
   1. In the Azure Portal go to **Settings** on the left, then **Environment variables**.
      1. They override all other settings in production
5. **IIS Environment Variables**



