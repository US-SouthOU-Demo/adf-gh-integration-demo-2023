# Azure Data Factory

Several steps are required to create a CI/CD workflow in a GitHub repository that is able to load an Azure DataFactory model, package it as an artifact, and publish that artifact to the production Azure DataFactory instances.  Below are instructions on how to configure Azure, the model Azure DataFactory instance, and GitHub to accomplish this.

1. [Connect Azure DataFactory to GitHub repository](./docs/01-connect-adf-github.md)
2. [Create Azure Active Directory App Registration that can be used by the GitHub repository](./docs/02-configure-app-registration.md)
3. [Give the App registration access to deploy resources to a Azure Resource Group](./docs/03-assign-permissions-to-app-registration.md)
4. [Configure GitHub with secrets required to use the Azure App Registration](./docs/04-configure-github-environments-secrets.md)

References
---
[https://learn.microsoft.com/en-us/azure/data-factory/continuous-integration-delivery-improvements](https://learn.microsoft.com/en-us/azure/data-factory/continuous-integration-delivery-improvements)
