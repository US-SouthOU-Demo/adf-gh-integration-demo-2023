# Assign Permissions to the App registration

In order for GitHub to use the App registration to deploy resources to Azure, the App registration will require permission
to view the Azure subscription, create new resources, and edit existing resources.  The following steps outline how to configure
Azure to allow the App registration access to the subscription

1. Go to the Azure portal [https://portal.azure.com](https://portal.azure.com)
2. Click the **Resource groups** icon
   - If the **Resource groups** icon is not shown, enter **Resource groups** in the search box and then click the **Resource groups** entry
3. In the subscription list, Click the link to the desired resource group
4. In the left-hand navigation menu, click **Access control (IAM)**
5. Click the **+ Add** button, a dropdown context menu will appear below the **+ Add** button
6. Select **Add role assignment**
7. Select the **Contributor** role
8. Click the **Next** button
9. For **Assign access to**, select **User, group, or service principal**
10. Click the **+ Select members** link
11. The **Select members** slide out will appear
12. In the **Select** textbox, enter the name of the App registration
13. Click the name of the App registration in the list
14. Click the **Select** button
15. Click the **Review + assign** button
16. Click the **Review + assign** button again

[Previous: Configure the Azure App Registration](./02-configure-app-registration.md)

[Next: Configure GitHub Environments and Secrets](./04-configure-github-environments-secrets.md)
