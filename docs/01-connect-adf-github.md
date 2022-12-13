# Configure Azure DataFactory to connect to GitHub repository

Azure DevOps or GitHub can be used as a source code repository for you Azure DataFactory instance.  The following steps outline
how to configure your Azure DataFactory to an existing GitHub repository.

1. Go to the Azure Porta [https://portal.azure.com](https://portal.azure.com)
2. Select the Azure DataFactory instance
3. Click the **Launch studio** button

![image](https://user-images.githubusercontent.com/102371320/207325293-65d1130d-a7ab-417e-b3b0-77e97e584501.png)

4. Azure DataFactory Studio will open in a new window
5. From the left-hand navigation bar, click the **Manage** button, which has a suitecase icon
6. In the left-hand navigation menu, under **Source control**, click **Git configuration**
7. Click the **Configure** button

![image](https://user-images.githubusercontent.com/102371320/207325522-be3826fd-8817-4427-b125-21d7a0eebb54.png)

8. The **Configure a repository** slide out panel will appear
9. In the **Repository type** textbox, select **GitHub**
10. In the **GitHUb repository owner** textbox, enter the name of your GitHub organization or user account which hosts the repository
11. Click the **Continue** button
12. A popup browser window will appear asking to authorize AzureDataFactory
13. Click the **AuthorizeDataFactory** button
14. If 2 factor authentication, 2FA, is enabled on your account, follow the steps to provide your 2FA pin code
15. The slide out panel will be updated
16. In the **Repository name** dropdown, select the repository
17. In the **Collaboration branch** dropdown, select **main** or another branch that you would like to use to store the code
18. In the **Publish branch** dropdown, select **adf_publish** or another branch that you would like to use to publish code from Azure DataFactory to GitHub
19. In the **Root folder** textbox, enter the name of the folder where the Azure DataFactory code should reside
    - the default is / but a subfolder can also be specified, for example **/AzureDataFactory/src/**
20. Check the **Import existing resources to repository** if your Azure DataFactory instance already contains Pipelines, Datasets, Data flows, Power Queries, etc.
    - In the **Import resource into this branch** textbox, enter the name of the branch to import the code from Azure DataFactory to on creation of the connection
21. Click the **Apply** button
22. The slide out panel will be updated to **Set working branch**
23. In the **Working branch** dropdown, select **main** or another branch that you would like to use to store the code
24. Click the **Save** button

Next|
---|
[Configure the Azure App Registration](./02-configure-app-registration.md)|
