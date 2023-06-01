# [Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/overview)

## What is included?

-   It enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs.
-   It supports both Linux and Windows systems.
-   You can develop in your favorite language, be it .NET, .NET Core, Java, Ruby, Node.js, PHP, or Python.
-   It offers automatic scaling and high availability.
-   It enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.
-   Deployment and management are integrated into the platform.
-   Endpoints can be secured.
-   Sites can be scaled quickly to handle high traffic loads.
-   The built-in load balancing and traffic manager provide high availability.

## Cost and Resources

-   You pay for the Azure compute resources your app uses while it processes requests based on the **App Service plan** you choose.
-   The App Service plan determines how much hardware is devoted to your host.

## Types of App Services

1. Web apps
    - App Service includes full support for hosting web apps.
1. API apps
    - Are much like Web apps. You get full Swagger support and the ability to package and publish your API in Azure Marketplace. The produced apps can be consumed from any HTTP- or HTTPS-based client.
1. WebJobs
    - You can use the WebJobs feature to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app.
    - They can be scheduled or run by a trigger.
    - WebJobs are often used to run background tasks as part of your application logic.
1. Mobile apps
    - It is used to build the backend of an iOS or Android app.
    - Easier to configure:
        - Store mobile app data in a cloud-based SQL database.
        - Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook.
        - Send push notifications.
        - Execute custom back-end logic in C# or Node.js.
    - On the mobile app side, there's SDK support for native iOS and Android, Xamarin, and React native apps.
