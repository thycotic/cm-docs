[title]: # (1.2.0 Release)
[tags]: # (release notes)
[priority]: # (894)
# 1.2.0 Release Notes

*Release Date: 2020-04-14*

## Enhancements

* Added ability to create a new Local Storage file (for Local Connections) directly from the Connection Manager Sign In dialog.
* Updated the User Interface so the Navigation section can be resized.
* Updated the general style for the Properties tab (bolding the headers, and text formats).
* When a large number of tabs are open, double-clicking on the left or right scroll arrows will jump to the far end of the tab list (in either direction).
* Added ability to login to Secret Server using the Secret Server web login (for SAML support).
* Added ability to launch Secret Server Secrets that use other Launcher types. Connection Manager will support any launcher that is supported by Secret Server and includes, but is not limited to: PowerShell, CmdLine, MS Word, Notepad, Excel. These launchers also support opening a tab in Connection Manager, session recording, and workflows.
* Added the ability to launch a Secret in the Secret Server UI and have the protocol handler open and run the launcher in Connection Manager. The Secret needs to be configured to use the protocol handler, and then launching it will use Connection Manager if it's available. When Connection Manager opens it will be in a "Locked" state where only the Secret Server launched session(s) are available.

  * If Connection Manager is launched using the protocol handler and is in the "Locked" state, users will have a "Sign In" option available to them to fully log into Connection Manager to use their other connections.
* Added support for two new Secret Server settings. Changing these settings in Secret Server will globally enforce the changes for Connection Manager applications that are connected. The Secret Server Settings are:

  * Allow Local Connections - Allows or disables the saving of credentials for any Local Connections. By default, this is set to Yes.
  * Allow Saving Credentials - Allows or disables the saving of credentials for any Secret Server connections. By default, this is set to Yes.

## Bug Fixes

* Fixed an issue, where if you selected the first row in the main Work area the context menu options (on right-click) did not display all of the available options.
* Fixed an issue, where if the Secret Server URL contained "v1" in the path it was replaced with "v2".
* Fixed an issue with Integrated connections (a local connection with a Secret Server Secret for credentials) where a Local SSH connection was retuning an "incorrect username or password" message if the Secret uses Secret Server Proxy.
