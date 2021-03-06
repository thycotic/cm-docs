[title]: # (CM Crash on Connection Change)
[tags]: # (secret server connection)
[priority]: # (702)
# Application Crash when Editing Existing Secret Server Connection

This topic reviews an issue that can cause an application crash for the Connection Manager 1.2.1 release, including what causes the issue and possible workarounds.

## Issue

In the Connection Manager 1.2.1 release a condition can be reached that causes the Connection Manager application to crash. There is no specific error message associated with the crash, but it occurs when the following conditions are met:

1. There is an existing connection to Secret Server.
1. The existing connection uses an **Authentication Type** of “Local Username/Password” and has the **Two Factor** option set to anything other than “None”.
1. The user edits the existing connection and changes the **Authentication Type** to “Web Login”.
1. The user tries to complete the web login connection.
1. The application crash occurs once the web login tries to store the login Token from Secret Server.

If the application crash occurs, the next time the user starts Connection Manager the Secret Server connection will be reset back to the original settings.

## Reason

In the Connection Manager 1.2.1 release, if the **Authentication Type** is set to “Local Username/Password” and the **Two Factor** option is set to anything other than “None”, the value of the **Two Factor** option is saved within the application. The crash occurs when Connection Manager receives the SAML Login token from Secret Server, but it is expecting one of the Local Two Factor options instead (like the “Pin Code”), and as a result cannot process the token and the application crashes.

## Workarounds

There are two possible workarounds for this issue.

### Workaround 1

1. Open Connection Manager and click “Edit” on the Secret Server connection you want to modify.
1. Keeping the **Authentication Type** as “Local Username/Password” click “Next”.
1. In the **Two Factor** option, change it to “None”.

   By setting the **Two Factor** option as “None” it forces Connection Manager to clear the expected value out from the settings so the conflict cannot occur.
1. Click the “Back” button on the bottom left to return to the previous screen.
1. Now, back on Step 1 of the Edit Secret Server connection dialog, you can change the **Authentication Type** value to “Web Login”.
1. You can now proceed with establishing the Web Login connection. Once the connect is made the new settings for the connection will be saved and the next time you log into this connection it will use the new settings

### Workaround 2

The second workaround option is about avoiding the issue initially instead of trying to “fix” the error state.

Instead of editing the existing connection users can create a totally new Secret Server connection using the “Web Login” option and specifying the remaining settings. They can then delete the previously existing connection to help ensure that the connections don’t get confused.

## Resolution

This issue will be resolved in the Connection Manager 1.3.0 Release.
