[title]: # (Connection Manager 1.0.0 Release Notes)
[tags]: # (releasenotes,1.0.0,newfeatures)
[priority]: # (801)

# Connection Manager 1.0.0 Release Notes

1.0.0 Release Notes

*Release Date: 2019-09-17*

This is for the initial release of Connection Manager. 

## New Features

Functionality in Connection Manager is broken down into two primary sections: Connection Manager – Free Tool and Connection Manager – Secret Server Integration.

## Connection Manager – Free Tool

### Remote Sessions

- Able to create ad-hoc connections for RDP sessions.
- Able to create ad-hoc connections for SSH sessions using PuTTY sessions.
- Encrypt and store the credentials and general connection information for any Local connections. 
- RDP Session - Add additional RDP session options (standard RDP options) when making a connection, including Windows Mode options (desktop size, color depth and auto window resizing) and Local Resource options (sharing of local devices, including audio).
- RDP Session - When editing a Local RDP connection, users should be able to change: the password, Windows Mode options and Local Resource options.
- SSH Session - Add additional SSH session options (standard SSH options) when making a connection, including Advanced SSH options (character set, font and font size).
- SSH Session - Add ability to specify a private key file and password to use when connecting to SSH session.
- SSH Session - Add ability to set and specify multiple Tunnel (using values for: Port, Destination server and Destination Port) for SSH sessions.
- SSH Session – When editing a Local SSH session, users should be able to change: the password, Advanced options (font size, type and character set), Private Key options and Tunnels.
- When Local sessions for RDP or SSH are launched the remote session will open as a new Tab in the work area.
- Remote sessions (RDP or SSH) have the ability to expand to a “Full Screen” mode.

### User Interface

- Added left-hand tree style navigation bar.
- Create Local folders to store, manage and sort Local connections.
- Added breadcrumb navigation to the top of the work area.
- RDP and SSH session types are marked by different colors for the tabs. 
- Added a Properties panel to the right inside the main work area when users select a connection or folder.
- In the properties panel for Local connections, allow users to view the password for that connection. 
- Local connections can be launched using two methods: Double-click on the connection row in the work area or click the launcher icon in the properties panel.
- Existing Local connections and folders can be edited by right-clicking on the row in the work area or by clicking an “Edit” button in the properties panel.
- When editing a folder under the Local connections section the folder name can be changed.
- Add ability to Remove any Local connections or folders.
- Added ability to view a list of any “Recent” sessions by selecting “Recent” in the navigation bar.
- Sessions can be launched by double-clicking on a connection in the “Recent” page. 
- Add ability to view a list/display of all active remote sessions on an “Active Session” page
- Show a screen view of a session on the Active Session page from the last time the session was accessed.
- Allow users to quickly navigate to a active session from the Active Session page by double-clicking on the session image.
- Add a scroll bar to the Tabs section of the work area so if multiple tabs are open and extend beyond the page, a user can scroll over to them.
- Add a Search bar to the top right of the work area so users can run a search on the current folder for a connection.

- Add a “Configuration” menu to the bottom of the navigation bar for application options.
- Make Global options for RDP and SSH sessions available for modification from the Configuration > Global Configuration option in the navigation bar.
- Add a set of Global RDP sessions options (using Windows Mode options and Local Resource options) that are used for new sessions by default.
- Add a set of Global SSH sessions options (using Advanced options [font size, type and character set], Private Key options and Tunnels) that are used for new sessions by default.
- Make Global options for RDP and SSH sessions available for modification from the Global Configuration option in the navigation bar.
- Add ability to Export existing Local connections and folders to an output file (JSON format).
- Make export action for Local connections available by right-clicking in the navigation bar or by right-clicking on a folder/connection in the workspace.
- When exporting a connection, users should have the option to include the Password (This will be in Clear Text so the file can be imported later).

- Add ability to Import a set of folders and connections (using the JSON format from the Export) under the Local Connections section. 
- Make the import action only available from the navigation bar.
- The import action should add all folders and connection details specified in the JSON file under the specific folder location that was selected when selecting the option. 

## Connection Manager – Secret Server Integration

### Integration

- Add ability to connect to a specific Secret Server instance (On-prem or Cloud).
- Add ability to add multiple Secret Server connections to a single Connection Manager instance.
- Display a list of all Secret Server connections under Configuration > Secret Server Connections.
- When connecting to Secret Server, allow for multi-factor login options (pin-code, duo push, duo phone call, none) to be used.
- When connecting to Secret Server add ability to select Secret templates to fetch for displaying Secrets. 
- When a connection is established with Secret Server the folder structure containing the Secrets that can be accessed for the logged in user should be displayed in the navigation bar. 
- Add ability to edit an existing Secret Server connection including the “friendly” name for the connection, password, domain field, multi-factor options and modify the list of templates. 
- Add ability to remove a Secret Server connection. 
- When selecting a Secret Server folder in the navigation bar, the work area should display all the Secrets and folders that are available to the user.

- Display a “Locked” icon when a Secret Server connection has not been authenticated and an “open lock” icon when it has been authenticated (for easy viewing).
- Add ability to launch a Secret with RDP or SSH credentials as a remote session similar to how Local connections are launched.
- When selecting a Secret from a Secret Server connection, do not display the Password field for the Secret in the properties panel. 
- ·    If a Secret doesn’t have all the necessary fields to launch a remote RDP/SSH session, a dialog should open that prompts the user to enter the missing values (like machine name/IP). 
- When selecting a Secret from a Secret Server connection, do not display the Password field for the Secret in the properties panel. 
- Add ability to support Secret Server workflows including Check-In/Check-Out, Change password on Check-In, Double Lock, Prompt for Reason or Ticket System, Request Access and Require Comment. 
- When accessing Secrets that use workflows, display a prompt for the workflow in the properties panel. 
- Add support for Session Recording that is set on Secrets from Secret Server following the standards that Secret Server uses for Session Recording.
- When viewing a Secret in the work area that has Session recording set in the Secret, display a “Record” indicator on the launcher icon in the properties panel.
- When launching a Session that has Session recording set in the Secret, display a “recording” icon in the session tab.
- ·    When Session recording for a remote session is active or completes, send all session information back to Secret Server for processing.
- When a Secret is accessed in Connection manager, send Audit information back to the specific Secret Server instance for logging purposes.