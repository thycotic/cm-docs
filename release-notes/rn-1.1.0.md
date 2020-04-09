[title]: # (1.1.0 Release)
[tags]: # (release notes)
[priority]: # (897)
# 1.1.0 Release Notes

_Release Date: 2020-01-08_

## New Features (for both Windows and macOS)

* Added ability to make an Integrated Connection: a Local Connection that uses a Secret from Secret Server for credentials.
* Added ability to perform Global Search when at the root for Local Connections or at the root of a Secret Server connection.
* Made loading of Folder, Connection, and Secret data dynamic when a folder is selected. 
* Displayed Personal Folders folder at the top of a Secret Server connection. 
* Added support for screen resolution size down to 1280x720. 
* Added ability to refresh a Secret Server connection or folder from the navigation bar. 
* Allow expanding and collapsing of Secret Server connections or Local Connections (at the root) in the navigation bar. 
* Included Computer Name value in the tab title and tab tool-tip pop-up. 
* Added support for a client PC running in FIPS mode. 
* On the Recent page, added a Connection Source column to identify if a connection is Local or from Secret Server. 
* On the Recent page, added a Connection Type column to identify whether Local Connection are SSH or RDP, or list the Secret template for Secret Server connections. 
* Secret connections from Secret Server will be listed on the Recent page.  
* When opening a Secret Server connection from the Recent page, a notification will be presented if the Secret has been deleted. 
* Secret connections that use the Check-In/Check-Out workflow will display a Check-In button if the Secret is currently checked out by the user. 
* The properties panel for Secret connections that use the Access Request workflow have been updated so the Access Request pop-up more closely matches the Access Request dialog from Secret Server. 
* If a Secret connection from Secret Server uses an empty white list, launching a connection will open a text box to enter a value. 
* If a Secret connection from Secret Server uses an SSH proxied session, Connection Manager will respect the Secret Server option to only record the SSH keystrokes from the session. 
* If no Secret Server connection exists in Connection Manager, opening the Secret Server Connections configuration will open directly to the Connect to Secret Server dialog. 
* Display user information message when a user has been disconnected from a remote session due to another user logging in. 
* Improved error message handling when attempting to create a connection to Secret Server. 
* When installing Connection Manager, allow for users to set a different location to store the local storage data file. 
* In the File menu for Connection Manager, added a quick link to the documentation. 

## Bug Fix

* Fixed an issue preventing users from seeing any Secrets listed at the root of a Secret Server connection.
