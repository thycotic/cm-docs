[title]: # (1.2.1 Release)
[tags]: # (release notes)
[priority]: # (893)
# 1.2.1 Release Notes

*Release Date: 2020-04-28*

## BUGS

* Fixed an issue for connecting to Secret Server using Multi-factor authentication (like DUO or RADIUS). The issue resulted with the message "Connection failed reason: A task was cancelled" and a failed connection after 20 seconds. The timeout setting for this authentication has been extended to 5 minutes.

### MacOS Specific

* Fixed an issue where some dialogs and settings options were not displayed correctly if the macOS system was set to Dark Theme.
