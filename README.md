## What Is This?

This is an example repo corresponding to multiple lessons within the LearnHowToProgram.com walkthrough on making API calls in C# in both a console app and an ASP.NET Core MVC app in [Section 5: Authentication with Identity](https://www.learnhowtoprogram.com/c-and-net/authentication-with-identity). The first lesson in the series is [Making an API Call with RestSharp](https://www.learnhowtoprogram.com/c-and-net/authentication-with-identity/making-an-api-call-with-restsharp).

There are multiple branches in this repo that are described more below.

Finally, note that these projects were scaffolded with the [`dotnet new`](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-new-sdk-templates) tool.

## How To Run This Project

### Install Tools

Install the tools that are introduced in [this series of lessons on LearnHowToProgram.com](https://www.learnhowtoprogram.com/c-and-net/getting-started-with-c).

### Get Developer API Key

This project uses the New York Times' Top Stories API to practice making API calls in C#. In order to use the Top Stories API, you'll need to create a free [New York Times developer account](https://developer.nytimes.com/). Follow the [Get Started](https://developer.nytimes.com/get-started) steps to create an application and get your own API key.

### Set Up and Run Project - Branches 1 and 2 Only

**The following setup instructions are for the branches `1_api_call_in_console_app` and `2_deserializing_responses_in_console_app` only.**

1. Clone this repo.
2. Open the terminal and navigate to this project's production directory. called "ConsoleApiCall".
3. Within the production directory "ConsoleApiCall", create a new file called `EnvironmentVariables.cs`.
4. Within `EnvironmentVariables.cs`, put in the following code, replacing the `[YOUR-API-KEY-HERE]` with your own New York Times API key. 

```csharp
namespace ConsoleApiCall.Keys
{
  public static class EnvironmentVariables
  {
    public static string ApiKey = "[YOUR-API-KEY-HERE]";
  }
}
```

5. Within the production directory "ConsoleApiCall", run `dotnet run` in the command line to start the project in development mode with a watcher.

### Set Up and Run Project - Branch 3 Only

**The following setup instructions are for the branch `3_api_call_in_mvc_app` only.**

1. Clone this repo.
2. Open the terminal and navigate to this project's production directory. called "MvcApiCall".
3. Within the production directory "MvcApiCall", create a new file called `appsettings.json`.
4. Within `appsettings.json`, put in the following code, replacing the `[YOUR-KEY-HERE]` with your own New York Times API key. 

```json
{
  "NYT": "[YOUR-KEY-HERE]"
}
```

5. Within the production directory "MvcApiCall", run `dotnet watch run` in the command line to start the project in development mode with a watcher.
6. Open the browser to _https://localhost:5001_. If you cannot access localhost:5001 it is likely because you have not configured a .NET developer security certificate for HTTPS. To learn about this, review this lesson: [Redirecting to HTTPS and Issuing a Security Certificate](https://www.learnhowtoprogram.com/lessons/redirecting-to-https-and-issuing-a-security-certificate).

## Available Branches

**1_api_call_in_console_app**: This branch includes the code we added after working through the following lesson:

- https://www.learnhowtoprogram.com/c-and-net/authentication-with-identity/making-an-api-call-with-restsharp

**2_deserializing_responses_in_console_app**: This branch includes the code we added after working through the following lesson:

- https://www.learnhowtoprogram.com/c-and-net/authentication-with-identity/deserializing-api-responses-with-newtonsoft-json

**3_api_call_in_mvc_app**: This branch includes the code we added after working through the following lesson:

- https://www.learnhowtoprogram.com/c-and-net/authentication-with-identity/api-calls-in-an-asp-net-core-mvc-app
