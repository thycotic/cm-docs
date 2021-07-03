[title]: # (1.6.0 Release)
[tags]: # (release notes)
[priority]: # (888)

# 1.6.0 Release Notes

*Release Date: July 6, 2021*

>**Note**: Installer versions:
>
> * Windows: 1.3.0
> * macOS: 1.3.1

## New Features

* Organizations can now upload their own logo to replace the Thycotic logo in the Connection Manager application interface.

* Users can now customize the display of columns in the secret list window, including which columns are displayed, the width of each column, and the order in which items appear in each column (alphanumerical or reverse alphanumerical). The custom settings can also be saved together as a default.

* Users can now use Windows key combination shortcuts in an RDP session. These settings can be configured per connection or globally.

* Users can now search for secrets by templates because Connection Manager can now filter the list of secrets by the template selected.

## Automation and Improved Workflows

Connection Manager now provides guided workflows and automated default behaviors that simplify the processes of connecting to Secret Server and searching for secrets.

* If you begin to search for a secret but you have no active connection to Secret Server, Connection Manager reminds you to set up an active connection before your search can proceed. If you begin to search for a secret and you have active connections to Secret Server but you haven't chosen one, Connection Manager now automatically chooses an active connection for you.

* When a user initiates a connection using a secret that requires checkout, Connection Manager now presents a notification reminding the user to check in the secret when they are finished using it. This reminder is useful because if a user forgets to check a secret back in when they are finished, the secret will be unavailable to anyone else until the secret timer expires, which could be 24 hours or longer. This behavior mimics the user experience that Secret Server has provided for some time.

* In previous releases of Connection manager, once connected to Secret Server, the user had to decide on and manually select a folder in which to perform a search for their secret. Now Connection Manager automatically selects the top-most folder (connection) and performs an exhaustive downward search from there, covering every file in the folder selected, and every file in every level of subfolder all the way to the ends of the folder structure. This is already the default search behavior when mapping a secret to a local connection in the Mapping dialog.

   If the user selects a folder to begin their search, Connection Manager performs an exhaustive downward search from there, covering every file in the folder selected, and every file in every level of subfolder all the way to the ends of the folder structure.

* When connecting from previous releases of Connection Manager to Secret Server, users could select individual secrets to create connections from. Now users can also choose to select all secrets at once, then deselect any individual secrets that are not needed. This feature saves time for users who need to create initial connections using all or most secrets from a large collection of secrets.

* Users can now import RDP and SSH connections in CSV format from a file created in a third party platform including Devolutions, Microsoft Remote Desktop, and Royal TS. Connection Manager automatically detects the CSV file format, checks field mappings for ConnectionType, Name, Host, and CredentialUsername, concatenates the "CredentialsDomain" column with the "CredentialsUsername" column, and provides a confirmation message when the import is complete.

* Users can now pre-select Secret Server connections to automatically launch and authenticate on startup.

* Users can now use SSH Proxy to make a local connection to Secret Server using mapped credentials. Users already had this capability using RDP Proxy.

* When a user is launching multiple sessions simultaneously, Connection Manager now offers a one-click option to select a single launcher for all sessions.

* Users can now open more than one instance of Connection Manager per user on each server.

* For added security, administrators and users can now disable storage of connection credentials and passwords in a local data vault. When use of the local data vault is disabled, the user cannot create local RDP or SSH connections to servers. When the local vault is already enabled and the user disables it, any existing local connections will be permanently deleted and the user will be unable to create new local connections. Users will only be able to access secrets that are synched from Secret Server. The user will not need to log into Connection Manager each time they open the application, but since they cannot save Secret Server connections or credentials locally, they will need to log into Secret Server when they open Connection Manager.

* Users can now use the same DAT file on Windows and Mac systems.

## Product Enhancements

* In the process for launching a single local connection/secret, the "Connect" action is now named "Launch Connection" in the interface.

* When a user is proxying from local connections, the name of the server connected to now appears first, in the following format:
**[ServerName] - Proxied over [DE Name]**

## Bug Fixes

* The name of the Connection Manager installer file is now correctly identified as `Thycotic.ConnectionManager.WindowsInstaller`

* Users can now use Web Login with Multi-Factor Authorization apps such as Duo without getting errors or multiple redirects.

* Users on Unix Mac machines can copy newline characters via SSH proxy and the characters are now preserved.

## Known Issues

* When using some versions of Connection Manager on a Mac to launch a secret through Secret Server, the connection fails. To fix this issue, try upgrading to the newest version of Connection Manager.

## Maintenance 

* Upgraded the embedded Chromium Browser to version 89.0.17 to support the latest stable channel of Chromium.

## General Information

* Connection Manager does not support Windows Server 2003.

* For Unicode characters, Connection Manager supports UTF-8 encoding.

* In Connection Manager 1.4.1, SSL certification check bypass is not possible for the web login method. This behavior is intentional.
