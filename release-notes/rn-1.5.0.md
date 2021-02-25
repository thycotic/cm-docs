[title]: # (1.5.0 Release)
[tags]: # (release notes)
[priority]: # (889)
# 1.5.0 Release Notes

*Release Date: March 2, 2021*

## Enhancements

* You can now select the drives you want to share in an RDP session instead of sharing all local drives.
* You can now customize the text and colors used in your SSH terminal interface.
* When connecting to Secret Server, the Generate Token button is now automatically clicked in the background to generate the token for access.
* Terminology has been updated so that a list of allowed RDP connections is now called an *Allowed List* and a list of forbidden RDP connections is now called a *Blocked List*.
* When your internet connection to Secret Server is lost, Connection Manager now displays the dialog, Attempting to Auto-reconnect to [Secret Server name], with options to Cancel the attempt or to manually Reconnect. After a maximum of three minutes of unsuccessful attempts to reconnect, the dialog closes and the Connect dialog opens.  


## Bug Fixes

* When a user tries to delete, copy, cut, or paste a connection in a nested folder, Connection Manager now executes the command on the connection as expected.
* When a user creates a local RDP connection, maps it to a Secret Server Secret, then opens the connection, the tab header now displays the IP address of the target server instead of the proxy IP address.
* Resolved an issue with high CPU usage when using Connection Manager as protocol handler on Mac related to Secrets with Session Recording enabled.
* When a Mac user clicks on a Secret’s RDP launcher, logs into the Windows host, and sets the Windows host tab to full screen, Windows menu items are now available as expected.
* When a user adds a new Secret Server connection to a Secret Server Cloud instance, selects Web Login and clicks Next, Connection Manager now appropriately directs the user to the Web Login page for the Secret Server instance.
* Resolved application crashing by adding logic to better handle data imported via json and other file formats.
* Resolved an issue with high CPU usage when using Connection Manager as protocol handler on Mac related to Secrets with Session Recording enabled.
