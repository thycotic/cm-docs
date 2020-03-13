[title]: # (1.2.0 Release)
[tags]: # (release notes)
[priority]: # (894)
# 1.2.0 Release Notes

*Release Date: 2020-04-14*

## Enhancements

* Added ability to login to Secret Server using the Secret Server web login (for SAML support).
* Added ability to launch Secret Server Secrets that use other Launcher types. Connection Manager will support any launcher that is supported by Secret Server and includes, but is not limited to: PowerShell, CmdLine, MS Word, Notepad, Excel. These launchers also support opening a tab in Connection Manager, session recording, and workflows.
* Added the ability to launch a Secret in the Secret Server UI and have the protocol handler open and run the launcher in Connection Manager. The Secret needs to be configured to use the protocol handler, and then launching it will use Connection Manager if it's available. When Connection Manager opens it will be in a "Locked" state where only the Secret Server launched session(s) are available.

  * If Connection Manager is launched using the protocol handler and is in the "Locked" state, users will have a "Sign In" option available to them to fully log into Connection Manager to use their other connections.
* Added support for two new Secret Server settings. Changing these settings in Secret Server will globally enforce the changes for Connection Manager applications that are connected. The Secret Server Settings are:

  * Allow Local Connections - Allows or disables the saving of credentials for any Local Connections. By default, this is set to Yes.
  * Allow Saving Credentials - Allows or disables the saving of credentials for any Secret Server connections. By default, this is set to Yes.

## Bug Fixes

* Fixed an issue where if the Secret Server URL contained "v1" in the path it was replaced with "v2".
* Fixed an issue with Integrated connections (a local connection with a Secret Server Secret for credentials) where a Local SSH connection was retuning an "incorrect username or password" message if the Secret uses Secret Server Proxy.
