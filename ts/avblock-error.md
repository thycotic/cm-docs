[title]: # (AVBlock Error with Session Recording)
[tags]: # (session recording)
[priority]: # (703)
# AVBlock Error with Session Recording

In Connection Manager when attempting to launch a Secret Server Secret that has session recording enabled, the session may fail to launch and return an exception error in the logs. 

Examples of these error exceptions:

* ERROR Thycotic.ConnectionManager.Core.ViewModels.ExplorerViewModel: Unhandled exception in Connect: Autofac.Core.DependencyResolutionException: An exception was thrown while activating Thycotic.ConnectionManager.SecretServer.SecretServerSessionBackgroundWork.

* ERROR Thycotic.ConnectionManager.Core.Managers.ErrorProcessingManager: Show error to user: An exception was thrown while activating Thycotic.ConnectionManager.SecretServer.SecretServerSessionBackgroundWork.

## Problem

This is caused when a component that Connection Manager uses for session recording starts caching an invalid license for that component on the client machine. The invalid license causes an rdpwin.exe error for the recorded session when it launches, resulting in the error messages as shown in the examples above.

AVBlocks can call home to a licensing server, here `https://lms.primosoftware.com/`, from the client endpoint where the Protocol Handler is installed and it creates a local cache of the licence in `%temp%\primosoftware.lm.cache`.

If the access to the license server is then blocked, the cached license will eventually expire and cause a PH recording error:

```bash
Failed to open transcoder: Error=Unlicensed feature Facility=AVBlocks, Code=9, Hint=vp8-enc;
```

This can be seen in 6.0.0.13 and newer logs with verbose logging enabled in `C:\Program Files\Thycotic Software Ltd\Secret Server Protocol Handler\log4net-rdp.xml`.

## Workaround

1. Re-enable access to https://lms.primosoftware.com/.
2. Delete the contents of `%temp%\primosoftware.lm.cache` for all affected users. <!--(this is assumed but untested) -->
