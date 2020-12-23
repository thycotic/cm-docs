[title]: # (Generate Log Entries)
[tags]: # (debug log entries)
[priority]: # (709)
# Generate Additional Log Entries

## Issue

In Connection Manager 1.4.1: if you need to generate additional log entries for troubleshooting, you can change the log level value to `DEBUG` and use the web login feature:

1.	Open the `Thycotic.ConnectionManager.exe.config` file

    (`C:\Program Files\Thycotic Software Ltd\Thycotic Connection Manager`)
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
