
Connect to Secret Server
========================

Connection Manager will only connect to Secret Server version 10.7 or later and
requires a valid Secret Server license.

1.  On the Configuration menu, select **Secret Server Connections**. If no
    Secret Server connections exist in Connection Manager, selecting the Secret
    Server Connections option will jump directly to Step 1: Connect to Secret
    Server. If other Secret Server connections exist, the Secret Server
    Connections window will open instead.

2.  On the **Secret Server Connections** window select **Add a Connection**. The
    Secret Server connection wizard opens.

![](media/ffa46fac82a28b1a2fac7b15c02c0896.png)

1.  Complete Step 1 required fields, including:

-   **Secret Server Name**: A friendly name for the connection.

-   **Secret Server URL**: The URL for the Secret Server instance, usually
    https://\<Server Name\>/SecretServer.

-   **Username**: The username for the Secret Server instance to which you want
    to login. (This is not the “username\@company.com” format.)

-   **Password**: The password for the account.

-   **Domain**: The Secret Server environment. If this environment has been
    given a specific Domain value for login, enter the same value here.

-   **Two Factor**: Select the appropriate two-factor authentication option for
    your environment.

-   **Remember me**: Select this check box if you want Connection Manager to
    remember the credentials you entered. This option stores the credentials in
    local storage and encrypts them using your application password.

**Note**: Even if the *Remember me* option is selected, a user will still need
to authenticate back to Secret Server when the application launches or times
out.

1.  After the required fields have been entered click **Connect**. Step 2 of the
    wizard opens.

![A screenshot of a cell phone Description automatically generated](media/79b6164180ee443e6b13018704ac4365.png)

In Step 2, the system automatically fetches a list of Secret templates from the
Secret Server URL entered in Step 1. The most common templates for RDP and SSH
sessions are selected by default. You may select and deselect additional
templates as needed, and you may also search for a specific template by name.

1.  Click **Finish** once all desired templates have been selected. The
    connection is added and appears in the navigation menu with a Lock icon to
    the left.

**Note**: Secret Server connections will persist between sessions of Connection
Manager; however, users must re-authenticate the connection after the
application is launched, or if the session times out.

Modify a Connection
-------------------

Existing connections to Secret Server can be modified. Most fields can be
modified except for the Secret Server URL field:

1.  On the Configuration menu, select **Secret Server Connections**. The Secret
    Server Connections window opens.

2.  Click **Edit** next to the Secret Server connection to be modified. The Edit
    text is between the Connection name and the URL value. The Connection dialog
    box opens.

![](media/f060ad35f61959fb45fd185cde153ff2.png)

**Note**: Users can make modifications to any of the fields here except for the
Secret Server URL. If the *Remember me:* option was selected previously, the
user will not be able to change the Username value either.

1.  Make any desired changes in Step 1 and click **Connect**.

![](media/4576c7f4dbdc6d91db636d502e6690b8.png)

1.  Make any desired changes in Step 2 and click **Finish**.

**Note**: A user may modify template selections at any time by selecting
**Edit** next to the Secret Server connection as shown below.

![](media/b76ffe8f41f280a935c6387f3732bdda.png)

Remove a Connection

To remove a connection:

1.  On the Configuration menu, select **Secret Server Connections**. The Secret
    Server Connections window opens.

2.  Click the **Remove** text to the far right of the Secret Server connection
    (as shown in the image above) to be removed. A warning prompt will ask you
    to confirm.

![](media/d48c70c8458ce426bcd56f378c481de9.png)

1.  Click **Yes** when finished.

Import and Export Connections
-----------------------------

### Export Connections

Export allows users to export all local connections. When a folder is selected,
the contents of that folder, along with any subfolders (and their contents), are
included in the export file.

To initiate an export, perform the following:

1.  On the Navigation menu, click the **desired folder or connection** under the
    Local connection section. Alternatively, the Local connection or folder may
    be selected in the main window.

2.  Right-click and select **Export**. The Select file to export window opens.

![](media/b6603ab7c2ec4dbf6ee7a8f05bbff7e2.png)

1.  Click **Browse** and enter **the location and file name** for export.

**Note**: If Export Password(s) is selected, passwords for the connections is
exported in **clear text**.

1.  Click **Export** to complete the action.

The Import option is only available for Local connections and can only be
accessed from the Navigation tree.

### Import Connections

To initiate an import, perform the following:

1.  On the Connection Manager navigation tree, select the **Local Connection
    folder** to which the contents should be imported.

2.  Right-click and select **Import**. A file browser window opens.

3.  Navigate to the location of the JSON file containing the content for import.

4.  Select the **file** and click **Open**. The Connections are imported.

### File Format 

The contents of any Export or Import file is in JSON format. The following is an
example of the formatting:

![A picture containing screenshot Description automatically generated](media/f6fd273acc8e08fb4a7f6614a4ae316f.png)

**Note**: The red text for the password field indicates that this part of the
JSON file will only be included if the Export Password(s) option is used.

Configure Global Settings
=========================

Global Settings allows a user to control default parameter values when creating
Local connections. To access:

1.  On the Configuration menu, click **Global Settings**. The Global
    Configurations dialog box opens.

![A screenshot of a cell phone Description automatically generated](media/10cc4df31eb11f27e0059ce24450cd57.png)

The available options are accessible via tab controls and include RDP Global
Settings and SSH Global Settings:

-   These default options may be overridden within the individual connections.

-   Connections from Secret Server do not support all available parameters. In
    such cases the default parameters will be substituted.

-   Any of the default configuration values that are specified in a Secret, from
    a Secret Server connection, will use the values from the Secret instead of
    the Global Configurations.

Common User Activities
======================

Since there are many variations and configuration options for remote
connectivity, it is not possible to cover all of them in detail. However,
Connection Manager does support many of these variations. Feel free to explore
further and if you have additional questions please [contact
support](https://thycotic.force.com/support/s/contactsupport).

Create a New Folder
-------------------

Connection Manager uses folders to help organize local connections.

1.  Navigate to the **location where a new folder should be created**.

2.  Right-click and select **New Folder**.

![](media/91efa9bfcfff54e56578142c4d2a6df7.png)

1.  Enter the **Folder Name** and click **Create**.

2.  Choose the appropriate **credential option** from the list:

-   **None**: No credential values will be set or required for the new folder.

-   **Local Credentials**: Allows a user to create the credentials for the new
    folder.

-   **Inherit from Folder**: Allows a user to set credentials for a sub-folder
    to imitate the folder in which it will reside.

-   **Map Secret**: Allows a user to apply secrets to the new folder.

View [Integrated Connections](#create-an-integrated-connection) for additional
information on credentials.

Edit a Folder
-------------

1.  Navigate to the **folder to be edited** and right-click. The Edit Folder
    dialog box opens.

![A screenshot of a cell phone Description automatically generated](media/7d167076d6416998e2f20f60bf285f99.png)

1.  Make any desired change to the folder and click **Save**.

View the [Integrated Connections](#create-an-integrated-connection) section for
additional information on credentials.

Delete a Folder
---------------

When a folder is deleted, the folder and its contents (Local connections and
other folders) are deleted.

**Important**: This action is **not** reversible. Once a connection is deleted
it cannot be recovered.

1.  Navigate to the **folder to be deleted**.

2.  Right-click the **folder name** and select **Delete**. A confirmation window
    opens.

![](media/63f844ab47b574a4854bc450b6620dd3.png)

1.  Select **Yes** to continue.

Create a New Connection to Remote Systems
-----------------------------------------

Connection Manager allows users to create new connections to remote systems and
store them locally. Secret Server Secrets may only be viewed and initiated
within Connection Manager.

All required fields and the appropriate optional fields must be filled out. If
you choose not to enter a username and password, you will be prompted to enter
this information when connecting. Many of the fields will have default values
pre-entered. You may keep these values or modify them as appropriate.

1.  From the Local connections section of the navigation tree, navigate to the
    **folder where the new connection will be created**.

2.  Right-click the **folder name** and select **New Connection** followed by
    the **connection type** (RDP or SSH).

Dependent upon the connection type (RDP or SSH), a dialog box will open. The
options will vary based on the type of connection selected. View [Integrated
Connections](#create-an-integrated-connection) for additional information on
credentials.

**RDP Connection**

-   **Connection Name**: Enter a friendly name for the new connection.

-   **Computer Name**: Enter the unique identifier for the computer name or IP
    address.

-   **Port**: Enter the port number for the connection or leave default.

-   **Credentials**: Select the appropriate credential for the new connection.

![](media/f7838f4ff70859bd55183f9dae7364e9.png)

**SSH Connection**

-   **Connection Name**: Enter a friendly name for the new connection.

-   **Computer Name**: Enter the unique identifier for the computer name or IP
    address.

-   **Port**: Enter the port number for the connection or leave default.

-   **Credentials**: Select the appropriate credential for the new connection.

![](media/f6dfadc3c855184518992a0864194ccf.png)

**Note**: The default value settings may be modified under the Configuration
option.

1.  Once all appropriate information is added, click **Create** to add the
    connection.

Create an Integrated Connection
-------------------------------

When logging into Connection Manager, if there are no existing Secret Server
connections, a user will be directed to the Create a Secret Server Connection
dialog box as shown in the [Connect to Secret Server](#connect-to-secret-server)
section.

### Credentials

Users can apply credentials directly to new folders and connections and at the
same time, ensure all sub-folders inherit the same credentials.

-   **None**: Allows a user to create new folders and connections without any
    credentials – i.e. no username and password values. This can be changed
    later.

-   **Local Credentials**: Allows a user to apply username and password
    credentials to the new folder or local connection.

![](media/df9b7e7008840c804176a2f505bff56b.png)

-   **Inherit from Folder**: Allows a user to apply credentials or a secret to a
    folder or connection to imitate the folder in which it will reside, or any
    sub-folders or connections created within it. While making the connection,
    if a connection already exists, it will be displayed.

![](media/b5598b7bf0c3add5b0e70092dc982fd0.png)

-   **Map Secret**: Allows a user to apply secrets to the new folder or
    connection.

![](media/c1a92d8d5b1644a536379e3df5d96d7a.png)

### Map a Secret to a Folder

Connection Manager gives a user the ability to map secrets directly to folders.

**Note**: The process is the same whether the connection is RDP or SSH.

1.  From within Connection Manager, [create a new folder](#create-a-new-folder)
    or [edit an existing folder](#edit-a-folder). The Create a Remote Desktop
    Connection dialog box opens.

2.  Enter the **connection name**, **computer name**, **port**, and from
    Credentials, select **Map Secret**. The Select Secret dialog box opens.

![A screenshot of a cell phone Description automatically generated](media/55107c0b6a3921af114e109b2b554b02.png)

The Select Secret dialog box shows all currently existing connections. Those
that are authenticated and immediately accessible, are shown with an open lock
next to the name. A closed lock indicated authentication is required, generally
a username and password. Users can drill-down the navigation tree to access more
folders.

Users may also search for a secret by name using the search bar at the top of
the Select Secret window. Clicking on a connection and then typing in the search
box will search only the folders within that connection.

1.  Click the **Secret** to which you would like to map and click **Select**.
    The name of the secret will now appear within the Create a Remote Desktop
    Connection dialog box under Connection Credentials.

![](media/9df71131c7ab6fabda6456cf4f3ebe94.png)

1.  Once all required information is entered, click **Create**.

Reauthenticate to Secret Server 
--------------------------------

When the application starts, any configured Secret Server connection will be
displayed but **not** connected.

To re-authenticate the Secret Server connection, double-click the **closed-lock
icon** in the navigation tree, or right-click and select **Connect**.

Edit Connections to Remote Systems
----------------------------------

1.  Navigate to the connection to be edited and click the **connection name**.

![](media/401f0f425e19633c408d3f3fda263d44.png)

1.  In the Connection properties area, click the **Edit button** under
    connection name. An Edit dialog will open depending on the connection type.

2.  Modify the fields as desired. (Most values in a local connection may be
    edited, except the required fields and the username field.)

3.  Click **Save** when finished.

Delete Connections from Remote Systems
--------------------------------------

A Local connection may be deleted from Connection Manager.

**Important**: This action is **not** reversible. Once a connection is deleted
it cannot be recovered.

1.  Navigate to the connection to be removed.

2.  Right-click the **connection** and select **Delete**. A confirmation dialog
    box will open.

![](media/fb2c3b70454117d7a1d34df3e8a819c4.png)

1.  Click **Yes** to confirm.

Open a Remote Connection
------------------------

The process of connecting to a Local connection or to a Secret from Secret
Server is essentially the same.

1.  Navigate to the remote connection. The remote session can be opened two
    ways:

-   In the main window, double-click the **connection name**. A new connection
    tab will open.

-   Select the **connection** to open the Properties tab. In the bottom half of
    the Properties window there is a section that lists available Launchers for
    use. Click the **desired launcher** and the session will open.

Sessions launched from a Secret Server Secret may have workflows associated with
the launching or closing of a session. If the connection requires no special
workflow, the remote connection will be established as a new tab in the work
area. If user entry is required for a workflow action, a window(s) will open
prior to connecting so users can enter the appropriate or required data.

**Note**: When connecting to a Secret with a whitelist, users will be prompted
to enter a text value if the whitelist is empty.

1.  Select a **launcher**. For Secrets where multiple launchers are available,
    you are prompted to select one.

![](media/e3e14a813a95a6ca1995446236e936a5.png)

1.  Select a **Host** or **Machine ID**. For Secrets where a host is not
    specified, you are prompted to enter one.

![A screenshot of a cell phone Description automatically generated](media/49425ed7e8827078a56d64c9c14e058f.png)

1.  Enter **user credentials**. For Connections or Secrets without an embedded
    username or password (or password), a dialog box opens (based on launcher
    type) to enter credentials.

![](media/364eb6628a19434d988ffc621e456a03.png)

Secrets with Workflows
======================

Connection Manager supports a variety of Secret Server workflows associated with
remote connections and the workflows functions are very similar to Secret Server
such as:

-   Require Comment

-   Check-in or Check-out (Able to check-in a secret if it was checked-out by
    the same user)

-   Change Password on Check-in

-   Prompt for Reason or Ticket System

-   Request Access

-   Double Lock

Users will see a notification in the properties area of the secret and if a
Secret has a workflow associated with it, Connection Manager will prompt you for
the appropriate workflow options in the Properties pane.. Please see the [Secret
Server Multi-Tier Secret Access
Workflow](https://thycotic.force.com/support/s/article/SS-HOW-EXT-Workflows).

Once the workflow is successful, the connection is established.

Related Resources
=================

-   [Secret Server Multi-Tier Secret Access
    Workflow](https://thycotic.force.com/support/s/article/SS-HOW-EXT-Workflows)

-   [Supported Characters for Machine Host
    Name](https://support.microsoft.com/en-us/help/909264/naming-conventions-in-active-directory-for-computers-domains-sites-and)

Need Help?
----------

[Open a support case](https://thycotic.force.com/support/s/contactsupport).
