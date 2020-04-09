[title]: # (Secret Server Requirements)
[tags]: # (faq,ss,apis,connection)
[priority]: # (705)
# Secret Server Requirements

## What are the quick, hard requirements for connecting to Secret Server?

* Must have Secret Server 10.7:

  * Requires RESTAPIs
* Must have the "IsConnectionManager" flag set on Secret Server license
* When we connect, we try to check what version of SS is being used:

  * If below 10.7 we will not connect
  * If we cannot detect the Secret Server version, we return the message we receive from SS and it usually means the Secret Server version # is hidden, and we receive an "Access Denied" message
* A Secret Server Username