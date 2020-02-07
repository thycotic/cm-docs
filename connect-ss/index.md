[title]: # (Connect to Secret Server)
[tags]: # (connect, secret server)
[priority]: # (300)

# Connect to Secret Server

Connection Manager will only connect to Secret Server version 10.7 or later and requires a valid Secret Server license.

1. On the Configuration menu, select **Secret Server Connections**. If no Secret Server connections exist in Connection Manager, selecting the Secret Server Connections option will jump directly to Step 1: Connect to Secret Server. If other Secret Server connections exist, the Secret Server Connections window will open instead.

2. On the **Secret Server Connections** window select **Add a Connection**. The Secret Server connection wizard opens.

     ![](images/connect-1.png)

3. Complete Step 1 required fields, including:

    - **Secret Server Name**: A friendly name for the connection.

     - **Secret Server URL**: The URL for the Secret Server instance, usually https://\<Server Name\>/SecretServer.

     - **Username**: The username for the Secret Server instance to which you want to login. (This is not the “username\@company.com” format.)

     - **Password**: The password for the account.

     - **Domain**: The Secret Server environment. If this environment has been given a specific Domain value for login, enter the same value here.

     - **Two Factor**: Select the appropriate two-factor authentication option for your environment.

     - **Remember me**: Select this check box if you want Connection Manager to remember the credentials you entered. This option stores the credentials in local storage and encrypts them using your application password.

   **Note**: Even if the *Remember me* option is selected, a user will still need to authenticate back to Secret Server when the application launches or times out.

4. After the required fields have been entered click **Connect**. Step 2 of the wizard opens.

   ![](images/connect-2.png)

   In Step 2, the system automatically fetches a list of Secret templates from the Secret Server URL entered in Step 1. The most common templates for RDP and SSH sessions are selected by default. You may select and deselect additional templates as needed, and you may also search for a specific template by name.

5. Click **Finish** once all desired templates have been selected. The connection is added and appears in the navigation menu with a Lock icon to the left.

   **Note**: Secret Server connections will persist between sessions of Connection Manager; however, users must re-authenticate the connection after the application is launched, or if the session times out.