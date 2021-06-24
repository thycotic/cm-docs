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

## Feature Updates

### Automation and Improved Workflows for Connecting to Secret Server

* To search for and find a secret, users must first be connected to Secret Server. In previous releases of Connection Manager, users had to first manually search for and select an active connection to Secret Server, and if they couldn’t find one after searching, they had to remember to manually create one.

   Now Connection Manager provides guided workflows and automated default behaviors that make this process much easier. If you begin to search for a secret without first choosing an active connection to Secret Server, Connection Manager automatically searches for and chooses an active connection for you. If you begin to search for a secret and you have no active connections to Secret Server, Connection Manager reminds you to set up an active connection before your search can proceed.

### Automation and Improved Workflows for Searching for Secrets

* In previous releases of Connection manager, once connected to Secret Server, the user had to decide on and manually select a folder in which to perform a search for their secret. Now the user can begin to search for a secret right away, without deciding on or selecting a folder. In this situation, Connection manager automatically selects the top-most folder (connection) and performs an exhaustive downward search from there, covering every file in the folder selected, and every file in every level of subfolder all the way to the ends of the folder structure. This is already the default search behavior when mapping a secret to a local connection in the Mapping dialog.

   If the user selects a folder to begin their search, Connection Manager performs an exhaustive downward search from there, covering every file in the folder selected, and every file in every level of subfolder all the way to the ends of the folder structure.

* When connecting from previous releases of Connection Manager to Secret Server, users could select individual secrets to create connections from. Now users can also choose to select all secrets at once, then deselect any individual secrets that are not needed. This feature saves time for users who need to create initial connections using all or most secrets from a large collection of secrets.

* Users can now import RDP and SSH connections in CSV format from a file created in a third party platform including Devolutions, Microsoft Remote Desktop, and Royal TS.

* Users can now pre-select Secret Server connections to automatically launch and authenticate on startup.

* Users can now use SSH Proxy to make a local connection to Secret Server using mapped credentials. Users already had this capability using RDP Proxy.

* When a user is launching multiple sessions simultaneously, Connection Manager now offers a one-click option to select a single launcher for all sessions.

* When a user initiates a connection using a secret that requires checkout, Connection Manager now presents a notification reminding the user to check in the secret when they are finished using it.

* Users can now open more than one instance of Connection Manager per user on each server.

* Administrators can now bypass encryption for the local vault database (DAT), thereby disabling local connection credentials and local vault passwords.

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
