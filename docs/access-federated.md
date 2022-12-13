# How to access Azure from GitHub Actions

In order to grant GitHub Actions workflows the ability to deploy Azure resources to Azure and code to those resources, 
this document will show how to create an App registration in Azure Active Directory and assign the permissions to enable 
GitHub Actions workflows to perform the deployments.

## Create an Azure App Registration

1. Go to the Azure portal [https://portal.azure.com](https://portal.azure.com)
2. Select Azure Active Directory
   - Either search for **Azure Active Directory** and then click the link, or

![image](https://user-images.githubusercontent.com/102371320/207109467-1dfff67a-8bfe-4cbc-998c-ae0f559e3c2c.png)

   - Click on the **Azure Active Directory** link under **Azure services**, if shown

![image](https://user-images.githubusercontent.com/102371320/207109541-9125211a-3673-446b-879d-6f7cef49454e.png)

3. In the left-hand navigation menu, under **Manage**, click **App registrations**
4. From the App registrations page, click the **+ New registration** button

![image](https://user-images.githubusercontent.com/102371320/207109946-3955e95c-d183-4436-9d9b-424d22749ea6.png)

5. Enter a name to help you identify your App registration
6. Select the supported account types
   - Single tenant should suffice
7. Click the **Register** button at the bottom
8. Once the App registration is created, the App registration details page will be displayed
9. In the left-hand navigation menu, under **Manage**, click **Certificates & secrets**
10. By default, the **Client secrets** tab will be selected, select the **Federated credentials** tab

![image](https://user-images.githubusercontent.com/102371320/207110260-ffea43ec-9895-4a74-bf18-3bdf41d078a1.png)

### Add Access to GitHub workflows to App registration

1. Click **+ Add credential** button
2. From the **Federated credential scenario** dropdown, select **GitHub Actions deploying Azure resources**
3. In the **Organization** textbox, enter the name of your GitHub organization
4. In the **Repository** textbox, enter the name of your GitHub repository
5. In the **Entity type** dropdown, select the appropriate value
   - Choose Environment if your workflow deploys using jobs that specify an environment; the environment name must also be entered
   - Choose Branch if your workflow is triggered by a push event to a specific branch or workflow_dispatch from a specific branch; the branch name must also be entered
   - Choose Pull request if your workflow is triggered by a pull_request event
   - Choose Tag if your workflow is executed for a specific tag; the tag name must also be entered
6. In the **Name** textbox, enter a descriptive name
7. Click the **Add** button

![image](https://user-images.githubusercontent.com/102371320/207110969-c1b22796-5cff-4ff5-a5fb-66236750ef48.png)

8. Repeat steps 1-7 for each environment, branch, tag as appropriate

