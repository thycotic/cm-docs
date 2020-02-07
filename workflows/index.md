[title]: # (Secrets with Workflows)
[tags]: # (secret, workflow)
[priority]: # (600)

# Secrets with Workflows

Connection Manager supports a variety of Secret Server workflows associated with remote connections and the workflows functions are very similar to Secret Server such as:

- Require Comment

- Check-in or Check-out (Able to check-in a secret if it was checked-out by the same user)

- Change Password on Check-in

- Prompt for Reason or Ticket System

- Request Access

- Double Lock

Users will see a notification in the properties area of the secret and if a Secret has a workflow associated with it, Connection Manager will prompt you for the appropriate workflow options in the Properties pane.. Please see the [Secret Server Multi-Tier Secret Access Workflow](https://thycotic.force.com/support/s/article/SS-HOW-EXT-Workflows).

Once the workflow is successful, the connection is established.