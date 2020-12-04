[title]: # (1.4.0 Release)
[tags]: # (release notes)
[priority]: # (890)
# 1.4.0 Release Notes

*Release Date: 15-December-2020*

## Enhancements

* Open and edit connections in bulk
  * by moving multiple connections into a folder and clicking the folder to open or edit all connections in the folder
  * by selecting multiple connections across multiple folders and clicking once to open of edit all the selected connections

* Move connection tabs:
  * Drag and drop tabs to reorder and organize them
  * Undock a tab from the main Connection Manager window as a standalone window. You can then move it to a different monitor, or re-dock the same tab next to the other tabs in the main Connection Manager window.

* Use multiple monitors for multiple RDP connections. The user can open an RDP session in full screen mode on a second monitor

* Reorganize Local Connections – Drag and drop folders within local connections

* Duplicate an existing connection, then rename it or save it in a different folder

* Edit local RDP or SSH connections in batch

* Ability to add/Admin or the Admin flag to remotely connect to an RDS server

* A new “Shared with me” section in the navigation lists all secrets/sessions that have been shared with you from a Secret Server connection

* For proxy connections, the remote host name appears on the session tab at the top of the screen to readily identify the machine it is associated with



## Bug Fixes

 * Renaming the default launchers in Secret Server no longer causes an error in Connection Manager on session launch

 * Connection Manager no longer freezes or crashes when SSH proxy is turned on in Secret Server

 * Users no longer receive frequent requests to re-authenticate while the RDP session is open

 * The Generate token button now works correctly after upgrading to a newer version

 * Connection Manager now displays the endpoint name when used as an RDP launcher

 * Connection Manager UI now appropriately restores to full screen and to the previously resized window

 * Connection Manager now supports "Proxied SSH process" launcher types

 * On the Connecting with an invalid certificate warning, Connection Manager now saves the selection to "bypass this error and connect anyway" (Mac OS)

 * When connecting to Secret Server, long template names are no longer truncated (Mac OS)
