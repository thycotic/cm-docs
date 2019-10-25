# Open a Remote Connection

The process of connecting to a Local connection or to a Secret from Secret Server is essentially the same. 

1. Navigate to the **remote connection**. The remote session can be opened two ways:

- From the main window, double-click the **connection name**. A new connection tab will open.
- Select **the connection** to open the Properties tab. In the bottom half of the Properties window there is a section that lists available Launchers for use. Click the **desired launcher** and the session will open.

Sessions launched from a Secret Server Secret may have workflows associated with the launching or closing of a session. If the connection requires no special workflo+-w, the remote connection will be established as a new tab in the work area. If user entry is required for a workflow action, a window(s) will open prior to connecting so users can enter the appropriate/required data.

## Select a Launcher

For Secrets where multiple launchers are available, you will be prompted to select one.  

![select-launcher](/select-launcher.png)

## Select a Host/Machine ID

For Secrets where a host is not specified, you will be prompted to enter one.  

![select-host](/select-host.png)

## Enter User Credentials

For Connections/Secrets without an embedded username/password (or password), a dialog box will open (based on launcher type) to enter credentials.  

![enter-user-creds](/enter-user-creds.png)

## Secrets with Workflows

Connection Manager supports a variety of Secret Server workflows associated with remote connections such as:

- Require Comment
- Check-in/Check-out
- Change Password on Check-in
- Prompt for Reason/Ticket System
- Request Access
- Double Lock

The workflow functionality is very similar to Secret Server. As a user you will see a notification in the properties area of the secret. Please refer to Related Resources for the Secret Server Multi-Tier Secret Access Workflow.

Depending on the type of workflow initiated, Connection Manager may prompt you with appropriate dialogue such as this for Approvals.

Once the workflow is successful the connection will be established. 