# Add a Connection

1. From the Configuration menu, select **Secret Server Connections**.
2. Select **Add a Connection**. The Secret Server connection wizard appears. 
3. In Step 1, fill out the required* fields including:

- **Secret Server Name** – A friendly name for the connection.
- **Secret Server URL** – The URL for the Secret Server instance. E.g.
   https://<Server Name>/SecretServer.
- **Username** –The username for the Secret Server instance to which you want to login. (This is not the “username@company.com” format.)
- **Password** – The password for the account.
- **Domain** – The Secret Server environment. If this environment has been given a specific Domain value for login, enter the same value here.
- **Two Factor** – Select the appropriate two-factor authentication option for your environment.
- **Remember me** – Select this check box if you want Connection Manager to remember the credentials you entered. This option stores the credentials in local storage and encrypts them using your application password. 

![conn-ss-step1](C:\Thycotic.ConnectionManager.Docs\how-to\images\conn-ss-step1.png)

**Note:** Even if selecting this option, the user will still need to authenticate back to Secret Server when the application launches or times out. 

4. After the required fields have been entered click **Connect**.

5. In Step 2, the system will automatically fetch a list of Secret templates from the Secret Server URL entered in Step 1. The most common templates for RDP and SSH sessions will be selected for you by default. You may select and deselect additional templates as desired. You may also search for a specific template by name. 


![conn-ss-step2](C:\Thycotic.ConnectionManager.Docs\how-to\images\conn-ss-step2.png)

6. Click **Finish** once all desired templates have been selected.


The connection will be added and will appear in the navigation menu with a “Lock” icon to the left.

 