This workflow uses the APIMatic API to generate a .NET SDK for the specified API and publishes it to nuget.org. In order to execute the workflow, you will first need to create the following repository secrets:

- APIMATIC_API_KEY: The Authentication key required to use APIMatic's API.
- NUGET_API_KEY: Your nuget.org API Key
- PACKAGE_NAME: The Name of your Nuget Package
- [Optional] PACKAGE_VERSION: The semantic version to be assigned to the package in the subsequent release. If this number is not provided, the workflow attempts to retrieve the current package version from nuget.org and increments the patch version. If the package is not yet published, it will be automatically assigned a version number of 1.0.1.

- Also add in your spec file in the "spec" folder of the repo.

With all the repository secrets and the spec file in place, trigger the workflow to generate and publish a Nuget package.
