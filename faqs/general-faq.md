# General Frequently Asked Questions

**Question**: Is there an associated Datasheet?

**Answer**: Yes, it's with Marketing. Please check with [Barbara Hoffman](mailto:mailtoBarbara.Hoffman@thycotic.com?subject=Connection Manager Datasheet) for a link.

 

**Question**: Is there a local session timeout for sessions within Connection Manager (CM)?

**Answer**:  Yes. For Local: Windows default socket connect timeout will apply (E.g. standard RDP/SSH remote session timeout). Session timeouts on secrets can be set in Secret Server (SS).

 

**Question**: I’m seeing a Connection failed error message while trying to connect to SS: “Connection failed reason: Request to Secret Server failed. Internal server error. An error has occurred.” What does this mean?

**Answer**: Seeing this error upon connection to SS means the currently installed version of SS is lower than 10.7.



**Question**: Is there a way to refresh the SS connections?

**Answer**: Not currently. An item has been added into the backlog for this and the team plans to look at it soon. Backlog: https://thycotic.visualstudio.com/Thycotic.ConnectionManager/_workitems/edit/144561 

 

**Question**: Where and how is the data for Connection Manager stored?

**Answer**: A Connection Manager data file containing the list of connections is stored in **C:\Users\\AppData\Roaming\Thycotic\Connection Manager.** The file is stored using AES 256 (256-bit) encryption.

 

**Question**: Is there support for SAML?                                         

**Answer**: Not currently. We use the REST APIs to communicate and they do not currently support SAML. 



**Question**: Is there a way to push scripted code out to multiple SSH sessions at one time for updates or commands? E.g. Is there a way to send a scripted file out to multiple PuTTY sessions at once using commands? 

**Answer**: There is currently no support to run this type of action from Connection Manager. This is sometimes done with X11, but we do not currently support that connection type. There is a Feature Request in the backlog to add support.  



**Question**: What happens if SS Heartbeat fails?

**Answer**: Connection Manager does monitor Secret Server heartbeat. If an active RDP/SSH session detects a heartbeat failure the session will be closed automatically.



**Question**: Is there any current performance data for Connection Manager? Including: general memory, amount of space needed, number of open connections that can be made at one time, etc.

**Answer**: We are getting more information. Currently we have tested with up to 30 open connections. Some of the performance numbers will depend on the system hardware for the machine that is running Connection Manager.  

 

**Question**: While recording a session, if a user isn’t on tab, what's the behavior? Do we reduce what we record and send? Or does it stay the same? the Can we tell if it's the "focus"?

**Answer**: We follow the same behavior as the SS session recording. If a user is not on the Tab, then we record and send less information. This uses the same code from SS. 
