[title]: # (1.5.0 Release)
[tags]: # (release notes)
[priority]: # (889)
# 1.5.0 Release Notes

*Release Date: March 2, 2021*

## Features

* Protocol Handler Improvements 
  * Administrator option to have Connection Manager register itself as the default Protocol Handler for all users 
  * Preserve the default Protocol Handler selection during an upgrade. 
  * Ability to have users switch between **Connection Manager**  and **Legacy Protocol Handler** 
  * Administrator option to install/uninstall the **Legacy Protocol Handler**  as the default for all users 
  * Ability for a non-admin user to switch between **Connection Manager**  and **Legacy Protocol Handler** 
* Customize the colors used in a SSH Session. 
  * Users will be able to choose colors used in an SSH session for the background, foreground, bold and underlined text 
  * Users will have a **Global Configuration** option as well as the ability to override and choose a different set of colors * for each local connection.  
  * Both Windows and Mac users will also be able to use the full color palette available on both systems.  
  * Users will be able to select from a preset color set or define a custom color set. 
  * Global configuration will be applied to new local connections only. Does not impact existing local connections or secret server connections. 
* Ability to choose local drives for mapping in an RDP session. 
  * Users will be able to select the drives they wish to map in an RDP session instead of choosing **All Drives** only.  
  * Global configuration will be applied to new local connections only. Does not impact existing local connections or secret server connections. 
* Auto-click the **Generate Token** button 
  * Added ability to automatically have **Generate Token** clicked for the user when connecting to Secret Server or when re-establishing a connection to make that process seamless to the customer. 
* Added capability to manage the connection to Secret Server during intermittent loss of internet connectivity. 
  * By setting a longer timeout if there is intermittent loss of internet connectivity, Connection Manager will hold on to the session allowing the user to resume without having to reconnect manually to secret server. 
  * Connection Manager will also automatically re-authenticate to Secret Server when connectivity has been re-established or give the user the option to manually re-authenticate. 
  * The reconnect notification dialog will be visible for about 3 minutes after which the dialog will close and the Connect dialog will open allowing the user to connect when internet connection has been re-established. 
* Enhanced searching in a machine list 
  * Users will be able to search from a long list of machine names and the list will filter as they type. Example typing “Ser” will narrow the results to all Server1, Server2 and Server3 
* Renamed *Whitelist* to *Allowed List* and *Blacklist* to *Blocked List*.  
  * To match the naming convention in Secret Server, we renamed the wording *Whitelist* in Connection Manager to *Allowed List* and *Blacklist* to *Blocked List*.  

## Maintenance 

* Upgraded FreeRDP library to 2.2.0 (Should resolve unexplained RDP connection interruptions in Connection Manager for Mac)  
* General Maintenance Updates 
  * Set copyright image to 2021 (Win/Mac) 
  * Resolved issues with a stuck connection with Connection Manager for Mac 
  * Added configuration option to disable automatic checking for update on startup. 
  * Set RDP session to stay in Full Screen mode after reconnecting if previous mode was full screen. 
  * A custom DAT file created in 1.4 will be usable in 1.5. 

## Bug Fixes 

* Resolved issues when the Mac app showed “null” certificate and the FreeRDP library crashes when connecting to a windows server (Mac)  
* Fixed an issue when mapping a local SSH connection to a Secret resulted in the error **A supplied password or username is incorrect**.
* Resolved unexplained RDP connection interruptions in Connection Manager for Mac 
* Resolved issues related to the Protocol Handler on a Mac. Full Screen and menu items now work with Protocol Handler (Mac)  
* Resolved an issue where the **Connect to Secret Server** dialog would hang if the connection was physically disconnected (Mac)  
* Resolved issues with High CPU utilization on a Mac (Mac) 
* Fixed issues related to Connection Manager crashing after a .json file import. 
* Resolved unrecoverable error connecting to Secret Server cloud via web login. 
* Fixed issues where Connection Manager could not switch back to the legacy protocol handler (Secret Server Launcher) for non-admin users.
* Resolved issues related to installing/uninstalling Connection Manager, using the legacy Protocol Handler (Secret Server Launcher) to launch secrets. Also see features under *Protocol Handler Improvements* above.

## Known Issues 

* Periodic black video in SSH session recording  
* RDP Connections may not stay open when connection manager auto-reconnects after a brief interruption in the internet connection. 
* Connection Manager not requesting a token refresh when TOTP is enabled.  
* In a Citrix environment when connecting via SSH Tunnel Proxy, you may in some cases get the error, **Failed to configure RDP component. The specified socket is already in use**.
* SSL Certificate bypass is not possible when using the Web Login method to connect to Secret Server. 
* Some users may get redirected to the Secret Server web page instead of Connection Manager when using the TOTP method and web login to connect to Secret Server or Secret Server cloud.  
* When used as a Protocol Handler, cannot open more than one instance per system. 
* When launching a secret from secret server on a Mac, connection fails with **Unexpected DTD declaration** error in the logs. 
