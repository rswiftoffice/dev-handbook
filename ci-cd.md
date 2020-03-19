# CI/CD

We strive to achieve full CI/CD implementation for all of our projects. With CI/CD, we can establish a consistent and automated way to build, package and test our applications. Furthermore, it reduces the workload of our devops members so they can focus on delivering higher priority projects.

It is best practice to implement your pipeline before your first release.

## Node.js

You can follow [Kevin's RTMA REST API](https://github.com/rswiftoffice/RTMA-api) which has tests, linting, styling and azure pipelines integrated already. Checkout release [v0.2.2](https://github.com/rswiftoffice/Wolfpack-api/tree/v0.2.2) for a barebones example.

## PHP

You can check out GLNM's Laravel deployment on Azure. Repository's on Github. 

For Laravel deployments:

- Have a .htaccess file in your root repository to redirect requests to public folder
```
<IfModule mod_rewrite.c>
    RewriteEngine on
    RewriteRule ^.*$ /public/$1 [NC,L,QSA]
</IfModule>
```

## Flutter (in-progress)

[View progress here](https://github.com/rswiftoffice/dev-handbook/issues/1).

## Azure Devops

You can use Azure Devops to build a pipeline for your applications. You can configure them through the [Devops portal](https://azure.microsoft.com/en-us/services/devops/) or manually through a yaml file.
