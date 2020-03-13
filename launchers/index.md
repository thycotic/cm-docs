[title]: # (Launchers)
[tags]: # (session recording)
[priority]: # (450)
# Launchers

Connection Manager can launch Secret Server Secrets that use other Launcher types. Connection Manager supports any launcher that is supported by Secret Server and includes, but is not limited to: PowerShell, CmdLine, MS Word, Notepad, Excel. These launchers also support opening a tab in Connection Manager, session recording, and workflows.

![session](images/session.png "Open launcher thumbnail and session recording indicator")

The Secrets with launcher can be launched in the Secret Server UI and have the protocol handler open and run the launcher in Connection Manager. The Secret needs to be configured to use the protocol handler, and when launched it uses Connection Manager if available. When Connection Manager opens it will be in a "Locked" state, with only the Secret Server launched session(s) being available.

If Connection Manager is launched using the protocol handler and is in the "Locked" state, users have a "Sign In" option available to fully log into Connection Manager to use their other connections.

![launcher list](images/launcher-list.png "Launcher list showing in Connection Manager")
