[title]: # (Generate Log Entries)
[tags]: # (debug log entries)
[priority]: # (709)
# Generate Additional Log Entries

Should you need to generate more detailed logging to help troubleshoot Connection Manager issues, you can set the log level to DEBUG per the steps below.
Setting the log level to DEBUG will generate larger log files so it is recommended that you return the setting back to INFO when you are done troubleshooting.

1.	Open the `Thycotic.ConnectionManager.exe.config` file

    (default location `C:\Program Files\Thycotic Software Ltd\Thycotic Connection Manager`)
2.	Find the snippet below and change `INFO` to `DEBUG.`

Before:
~~~~
    <root>
<level value="INFO" />
<appender-ref ref="LogFileAppender" />
<appender-ref ref="TraceAppender" />
</root>
~~~~
After:
~~~~
    <root>
<level value="DEBUG" />
<appender-ref ref="LogFileAppender" />
<appender-ref ref="TraceAppender" />
</root>
~~~~
