[title]: # (Generate Log Entries)
[tags]: # (debug log entries)
[priority]: # (709)
# Generate Additional Log Entries

## Issue

In the Connection Manager 1.4.1 release, Connection Manager might generate insufficient log entries for effective troubleshooting. To generate additional log entries such as entries for embedded web browser actions, you need to edit the Thycotic.ConnectionManager.exe.config file.

## Workaround

To generate additional log entries, set the log level value to DEBUG and use the web login feature:

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
