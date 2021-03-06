[title]: # (General)
[tags]: # (faq,error,failed,ss,connect,data,datasheet,SAML,help,heartbeat)
[priority]: # (701)

# General

## Is there a local session timeout for sessions within Connection Manager (CM)?

Yes. - For Local Connections, the Windows default socket connect timeout applies (e.g. standard RDP/SSH remote session timeout). The session timeouts on secrets can be set in Secret Server (SS).

## I'm seeing a Connection failed error message while trying to connect to SS

`Connection failed reason: Request to Secret Server failed. Internal server error. An error has occurred.`
Seeing this error upon connection to SS means the currently installed version of SS is lower than 10.7.

## Is there a way to refresh the SS connections?

Yes. - The Secret Server connection got a refresh button with the 1.2.0 version update.

## Where and how is the data for Connection Manager stored?

A Connection Manager data file containing the list of connections is stored in `C:\Users\\AppData\Roaming\Thycotic\Connection Manager`. The file is stored using AES 256 (256-bit) encryption.

## Is there a way to push scripted code out to multiple SSH sessions at one time for updates or commands?

Is there a way to send a scripted file out to multiple PuTTY sessions at once using commands?

There is currently no support to run this type of action from Connection Manager. This is sometimes done with X11, but we do not currently support that connection type. There is a Feature Request in the backlog to add support.  

## What happens if the SS Heartbeat fails?

Connection Manager does monitor Secret Server heartbeat. If an active RDP/SSH session detects a heartbeat failure the session will be closed automatically.

## Is there any current performance data for Connection Manager? Including: general memory, amount of space needed, number of open connections that can be made at one tie, etc.

We are getting more information. Currently we have tested with up to 30 open connections. Some of the performance numbers will depend on the system hardware for the machine that is running Connection Manager.  

## While recording a session, if a user isn't on tab, what's the behavior? Do we reduce what we record and send? Or does it stay the same? How can we tell if it's the "focus"?

We follow the same behavior as the Secret Server session recording. If a user is not on the Tab, then we record and send less information.