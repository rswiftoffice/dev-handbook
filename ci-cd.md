# CI/CD

We strive to achieve full CI/CD implementation for all of our projects. With CI/CD, we can establish a consistent and automated way to build, package and test our applications. Furthermore, it reduces the workload of our devops members so they can focus on delivering higher priority projects.

It is best practice to implement your pipeline before your first release.

## Node.js

You can follow [Kevin's Wolfpack rest API](https://github.com/rswiftoffice/Wolfpack-api) which has tests, linting, styling and azure pipelines integrated already. Checkout release [v0.2.1](https://github.com/rswiftoffice/Wolfpack-api/tree/v0.2.1) for a barebones example.

## Flutter applications

[Kevin](https://github.com/19hours) is working on a pipeline to build, package and upload flutter applications. 

Expected features include:

- On github release, build is triggered and code is tested and packaged.
- Server automatically screenshots and uploads them to stores.
- Set changelog descriptions.

## Azure devops

You can use azure devops to build a pipeline for your javascript or python applications. You can configure them through the [devops portal](https://azure.microsoft.com/en-us/services/devops/) or manually through a yaml file.
