# Step 6 - Import the Business Automation Application app

### Pepare the environment for the end-to-end scenario

1. Download the contents of the [following folder](Solution%20Exports/Business%20Automation%20Navigator).

2. Login to the **Navigator admin desktop** (URL should end with `desktop=admin`).

3. Click on **Connections** in the menu on the left.

   ![nav-connections](images/nav-connections.png)

4. Select the the **APPENGO** connection and click on the **Edit** button.

   ![nav-edit-appengo](images/nav-edit-appengo.png)

5. Click on the the **Connect...** button.

15. Click on the **Applications** tab.

16. Click on the **Import** button.

    ![nav-import-app](images/nav-import-app.png)

16. Choose the the previously downloaded file **ClientOnboardingRequest.zip** and click on the **Import** button. If an information dialog pops up after import, you can close it.

    **NOTE: **The target object store name specified in the Application is **BAWTOS**. If you are using a demo environment, the target store name could be different (eg: **TARGET**). In that case, the 2nd page of the application won't show any documents as it looks for the documents in the BAWTOS object store. To fix this, you can import the application template in Studio as instructed at the end of this page, and update the object store name there.

17. Click on the 3-dot menu for the **Client Onboarding** applicaiton and select **Details**,

18. Click on the **Permissions** tab.

19. Click on the **Add Teams** button.

20. In the popup, enter **#** in the **Filter by Teams** field and hit **Enter**.

    ![nav-app-permissions](images/nav-app-permissions.png)

21. Select the **#AUTHENTICATED-USERS** team and click on the right-facing arrow to move the team to the **Selected** column.

22. Click on the **Add** button.

23. Click on the **Close** button.

24. Close the **APPENGO** and **Connections** tabs at the top.

25. In the **Desktops** tab, click on the **Import** button.

26. Choose the the previously downloaded file **ICNExportedConfiguration.properties** and click on the **Import** button. You can close the summary dialog that pops up after the import is complete. Note that you may see a warning that says `The following items already exist on this system`. You can ignore this warning and continue with the import.

### Prepare a shared environment for labs

You only need to do these steps if your environment will be used to perform the labs associated with Client Onboarding.

1. Download the [application template twx file](Solution%20Exports/Business%20Automation%20Application/Client_Onboarding_Template.twx).

2. Login to **IBM Business Automation Studio**.

3. In the top-left corner, click on the menu icon and go to **Design** --> **Business applications**.

4. Click on the **Import** button.

5. Select the **Client_Onboarding_Template.twx** file that you previously downloaded and click on the **OK** button.

6. Once the import is complete, click on **Toolkits**.

7. Click on the tile for **Client Onboarding Toolkit** to open its details.

8. Click on the **Collaborators** tab.

9. Click on the **Add** button.

10. Select the **Group** radio button.

11. In the search box, enter the name of the shared user group (eg: cp4bausers).

12. Check the user group and click on **Add**.

    ![app-toolkit-collaborators](images/app-toolkit-collaborators.png)

13. In the top-left corner, click on the menu icon and go to **Design** --> **Business automations**.

14. Click on **Create** --> **External**.

15. Select **Business Automation Workflow** under **Select the connection type**.

16. Click on **Next**.

17. In the **Connection name** field, enter **External BAW System**.

18. In the **System URL** field, enter the host name of the BAW server that you previously used in navigator for the automation service (starting with `https://bawaut..`.

19. Enter the admin credentials and click **Next**.

20. In the **Select a process application** dropdown, select **Client Onboarding**.

21. Select the checkbox for **New Client Onboarding Request**.

    ![studio-external-aut-service](images/studio-external-aut-service.png)

22. Click on **Next**.

23. In the **Name** field, enter **Client_Onboarding_Workflows_External**.

24. Click on **Publish**.

Once you have imported the app successfully, [import the Business Automation Insights data](Step%207%20-%20Business%20Automation%20Insights.md).



