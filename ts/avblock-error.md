[title]: # (AVBlock Error with Session Recording)
[tags]: # (session recording)
[priority]: # (702)
# AVBlock Error with Session Recording

Connection Manager circumstantially throws an error message in cases when Session Recording is configured on a Secret.

## Problem

This is caused by caching expired Session Recording license on client computers. An expired license causes the rdpwin.exe error during session recording launches.

AVBlocks can call home to a licensing server, here `https://lms.primosoftware.com/`, from the client endpoint where the Protocol Handler is installed and it creates a local cache of the licence in `%temp%\primosoftware.lm.cache`.

If the access to the license server is then blocked, the cached license will eventually expire and cause a PH recording error:

```bash
Failed to open transcoder: Error=Unlicensed feature Facility=AVBlocks, Code=9, Hint=vp8-enc;
```

This can be seen in 6.0.0.13 and newer logs with verbose logging enabled in `C:\Program Files\Thycotic Software Ltd\Secret Server Protocol Handler\log4net-rdp.xml`.

## Workaround

1. Re-enable access to https://lms.primosoftware.com/
2. Delete the contents of `%temp%\primosoftware.lm.cache` for all affected users <!--(this is assumed but untested) -->
