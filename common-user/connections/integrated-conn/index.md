[title]: # (Integrated Connection)
[tags]: # (connection, integrated)
[priority]: # (507)
# Create an Integrated Connection

When logging into Connection Manager, if there are no existing Secret Server connections, a user will be directed to the Create a Secret Server Connection dialog box as shown in the [Connect to Secret Server](../../../connect-ss/index.md) section.

## Credentials

Users can apply credentials directly to new folders and connections and at the same time, ensure all sub-folders inherit the same credentials.

* __None__: Allows a user to create new folders and connections without any credentials – i.e. no username and password values. This can be changed later.
* __Local Credentials__: Allows a user to apply username and password credentials to the new folder or local connection.

  ![Local Credentials](images/integrated-1.png "Local Credentials modal")
* __Inherit from Folder__: Allows a user to apply credentials or a secret to a folder or connection to imitate the folder in which it will reside, or any sub-folders or connections created within it. While making the connection, if a connection already exists, it will be displayed.

  ![Inherit](images/integrated-2.png "Inherit from folder modal")
* __Map Secret__: Allows a user to apply secrets to the new folder or connection.

  ![Map](images/integrated-3.png "Allow secrets mapping to new connection/folder")

## Map a Secret to a Folder

Connection Manager gives a user the ability to map secrets directly to folders.

>**Note**: The process is the same whether the connection is RDP or SSH.

1. From within Connection Manager, [create a new folder](../../folder.md#create_a_new_folder) or [edit an existing folder](../../folder.md#edit_a_folder). The Create a Remote Desktop Connection dialog box opens.
1. Enter the __connection name__, __computer name__, __port__, and from Credentials, select __Map Secret__. The Select Secret dialog box opens.

   ![Select](images/integrated-4.png "Select Secrets to map")

   The Select Secret dialog box shows the currently existing connections. Those that are authenticated and accessible, are shown with an open lock next to the name. A closed lock indicated authentication is required, generally a username and password. Users can drill-down the navigation tree to access more folders.

   Users may also search for a secret by name using the search bar at the top of the Select Secret window. Clicking on a connection and then typing in the search box will search only the folders within that connection.
1. Click the __Secret__ to which you would like to map and click __Select__. The name of the secret will now appear within the Create a Remote Desktop Connection dialog box under Connection Credentials.

   ![Credentials](images/integrated-5.png "Credentials modal")
1. Once all required information is entered, click __Create__.
