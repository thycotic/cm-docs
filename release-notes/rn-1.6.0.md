[title]: # (1.6 Release)
[tags]: # (release notes)
[priority]: # (888)

# 1.6.0 Release Notes

*Release Date: July 6, 2021*

## New Features

* For added security, administrators and users can now disable storage of connection credentials and passwords in a local data vault. When the local data vault is disabled, the user cannot create local RDP or SSH connections. When the local vault is already enabled and the user disables it, any existing local connections are permanently deleted and the user will only be able to access secrets that are synched from Secret Server. The user will not need to log into Connection Manager each time they open the application, but they will need to log into Secret Server when they open Connection Manager.

* Users can now import RDP and SSH connections in CSV format from a file created in a third party platform, including Devolutions, Microsoft Remote Desktop, and Royal TS. Connection Manager automatically detects the CSV file format, checks field mappings for ConnectionType, Name, Host, and CredentialUsername, concatenates the "CredentialsDomain" column with the "CredentialsUsername" column, and provides a confirmation message when the import is complete.

* Users can now customize the display of columns in the secret list window, including which columns are displayed, the width of each column, and the order in which items appear in each column (alphanumerical or reverse alphanumerical). The custom settings can also be saved together as a default.

* Users can now use SSH Proxy to make a local connection to Secret Server using mapped credentials,a capability previously available only for RDP Proxy.

* Users can now use Windows key combination shortcuts in an RDP session. These settings can be configured per connection or globally.

* Organizations can now upload their own logo to replace the Thycotic logo in the Connection Manager application interface.

* Users can now pre-select Secret Server connections to automatically launch and authenticate on startup.

* Users can now create and edit secrets in Secret Server using a link in Connection Manager.

* Users can now search for secrets by the template they are based on.  

## Automation and Improved Workflows

Connection Manager now provides guided workflows and automated default behaviors that simplify the processes of connecting to Secret Server and searching for secrets.

* In previous releases of Connection manager, the user could not search for a secret without first selecting a folder to search in. Now Connection Manager automatically selects the top-most folder (connection) and performs an exhaustive downward search from there, covering every file in the folder selected, and every file in every level of subfolder. This is already the default search behavior when mapping a secret to a local connection in the Mapping dialog. If the user selects a folder to begin their search, Connection Manager performs an exhaustive downward search from there.

* When connecting from previous releases of Connection Manager to Secret Server, users could select individual secrets to create connections from. Now users can also choose to select all secrets at once, then deselect any individual secrets that are not needed. This feature saves time for users who need to create initial connections using all or most secrets from a large collection of secrets.

* When a user initiates a connection using a secret that requires checkout, Connection Manager now presents a notification reminding the user to check in the secret when they are finished using it. This behavior, which mimics the user experience that Secret Server has provided for some time, helps to prevent secrets from being unnecessarily unavailable to others for 24 hours or longer.

* If you begin to search for a secret and you have active connections to Secret Server but you haven't chosen one, Connection Manager now automatically chooses an active connection for you. If you begin to search for a secret but you have no active connection to Secret Server, Connection Manager reminds you to set up an active connection before your search can proceed.

* When a user is launching multiple sessions simultaneously, Connection Manager now offers a one-click option to select a single launcher for all sessions.

* Users can now open more than one instance of Connection Manager per user on each server.

* Users can now use the same DAT file on Windows and Mac systems.

## Product Enhancements

* In the process for launching a single local connection/secret, the "Connect" action is now named "Launch Connection" in the interface.

* Under Global Configurations, a *Preferences* tab has been added enabling users to choose how server names and secret names appear on tabs and thumbnails.

* When a user is proxying from local connections, the name of the server connected to now appears first, in the following format:
*[ServerName] - Proxied over [DE Name]*

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
