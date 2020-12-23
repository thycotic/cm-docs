[title]: # (Generate Log Entries)
[tags]: # (debug log entries)
[priority]: # (709)
# Generate Additional Log Entries

If you need to generate additional log entries to help troubleshoot Connection Manager issues, you can set the log level to DEBUG. Bear in mind that the DEBUG setting will generate many more log entries and larger log files, so after troubleshooting
you should return the log level to its default setting, INFO.

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
