[title]: # (1.4.1 Release)
[tags]: # (release notes)
[priority]: # (890)
# 1.4.1 Release Notes

*Release Date: 15-December-2020*

## Enhancements

* Users can now open connections in bulk by selecting multiple connections across multiple folders and clicking once to open them all, or by moving multiple connections into a folder and clicking the folder once to open all connections in the folder.

* Users can now click and drag a session tab to undock it from the main Connection Manager window. The tab becomes a standalone window that users can move to a different monitor or to a different position on their desktop. Users can also re-dock the window as a tab next to any of the other tabs in the main Connection Manager window.

* Users can now open an RDP session in full screen mode on a second monitor.

* Users can now reorganize Local Connections by dragging and dropping folders.

* Users can now duplicate an existing connection using copy/paste, then rename it or save it in a different folder.

* Users can now edit Local RDP or SSH connections in bulk.

* Added Run as Admin support for RDP sessions.

* A new “Shared with me” section in the navigation lists all secrets/sessions shared with you from a Secret Server connection.

* When a session is connecting using a proxy, the remote host name appears on the session tab at the top of the screen.

* Users can now enable the microphone option on an RDP connection (not the same as session recording)

* Devolutions import now provides improved error message handling.

* Users can now see the Secret name on the Select Launcher dialog.

* Users can now mark multiple items as Favorites using the Context menu.

* An icon has been added to the Connection tab for maximizing the window.


## Bug Fixes

* Renaming the default launchers in Secret Server no longer causes an error in Connection Manager on session launch.

* Connection Manager no longer freezes or crashes when SSH proxy is turned on in Secret Server.

* Users no longer receive frequent requests to re-authenticate while the RDP session is open.

* The Generate token button now works correctly after upgrading to a newer version.

* Connection Manager now displays the endpoint name when used as an RDP launcher.

* Connection Manager UI now appropriately restores to full screen and to the previously resized window.

* Connection Manager now supports "Proxied SSH process" launcher types.

* On the Connecting with an invalid certificate warning, Connection Manager now saves the selection to "bypass this error and connect anyway" (Mac OS).

* When connecting to Secret Server, long template names are no longer truncated (Mac OS)

* Fixed an issue related to exporting local connection folders.


## Known Issue

* Clicking on “X” to close an undocked session window, then immediately trying to move the window back to the docking area could lock the other tabs.
Workaround: Close and re-start Connection Manager.
