# Adding Secrets & Environments to Repository

## Adding Environments

1. Go to the repository in Github
   - ie, https://github.com/[organization]/[repository]
2. From the top navigation bar, click the **:gear: Settings** tab
3. In the left-hand navigation, under **Code and automation**, click **Environments**
4. Click the **New environment** button
5. In the **Name** textbox, enter the name for the environment
6. Click the **Configure environment** button
7. If the environment requires gated approvals, 
   - Click the **Required reviewers** checkbox
   - Add the name(s) of the user(s) or team(s) who should be able to approve the deployment
8. Additional protection can be added by 
   - Changing the **Deployment branches** dropdown to **Selected branches**
   - Click the **+ Add deployment branch rule** link
   - In the Branch name prefix, enter the name of the branch
   - Click the **Add rule** button

## Adding Environment Secrets

1. From the Environments page
2. Click the **+ Add secret** link
3. In the **Name** textbox, enter the name of the secret
   - Names must be all upper-case; if a name with lower-case characters is entered, it will automatically be converted to all upper-case when saved
4. In the **Value** textbox, enter the value of for the secret
   - Note that once you save the value of the secret, you will not be able to see that value in GitHub again

## Adding Repository Secrets

1. From the Repository page
2. From the top navigation bar, click the **:gear: Settings** tab
3. In the left-hand navigation, under **Security**, expand **Secrets**, click **Environments**
4. Click the **+ Add secret** link
5. In the **Name** textbox, enter the name of the secret
   - Names must be all upper-case; if a name with lower-case characters is entered, it will automatically be converted to all upper-case when saved
6. In the **Value** textbox, enter the value of for the secret
   - Note that once you save the value of the secret, you will not be able to see that value in GitHub again

