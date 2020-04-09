[title]: # (Connection to Remote Systems)
[tags]: # (connection, remote)
[priority]: # (503)
# Create a New Connection to Remote Systems

Connection Manager allows users to create new connections to remote systems and store them locally. Secret Server Secrets may only be viewed and initiated within Connection Manager.

All required fields and the appropriate optional fields must be filled out. If you choose not to enter a username and password, you will be prompted to enter this information when connecting. Many of the fields will have default values pre-entered. You may keep these values or modify them as appropriate.

1. From the Local connections section of the navigation tree, navigate to the folder where the new connection will be created.
1. Right-click the __folder name__ and select __New Connection__ followed by the __connection type__ (RDP or SSH).

   Dependent upon the connection type (RDP or SSH), a dialog box will open. The options will vary based on the type of connection selected. View [Integrated Connections](../integrated-conn/index.md) for additional information on credentials.

   __RDP Connection__

      * __Connection Name__: Enter a friendly name for the new connection.

      * __Computer Name__: Enter the unique identifier for the computer name or IP address.

      * __Port__: Enter the port number for the connection or leave default.

      * __Credentials__: Select the appropriate credential for the new connection.

   ![RDP](images/remote-1.png "RDP Connection page")

   __SSH Connection__

      * __Connection Name__: Enter a friendly name for the new connection.

      * __Computer Name__: Enter the unique identifier for the computer name or IP address.

      * __Port__: Enter the port number for the connection or leave default.

      * __Credentials__: Select the appropriate credential for the new connection.

   ![SSH](images/remote-2.png "SSH Connection page")

   >**Note**: The default value settings may be modified under the Configuration option.
1. Once all appropriate information is added, click __Create__ to add the connection.
