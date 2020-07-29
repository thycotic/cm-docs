[title]: # (1.3.0 Release)
[tags]: # (release notes)
[priority]: # (892)
# 1.3.0 Release Notes

*Release Date: 2020-07-28*

>**Note**: The macOS installer will be made available as a 1.3.1 installer in the next couple of days.

## Enhancements

* Ability to import connections from third party platforms in CSV format.
  * Adding option to import from CSV.
  * Includes “Import” dialog which allows mapping of fields in CSV to Connection Manager fields.
  * Imported connections import as Local connections.
  * Import can generate 2 reports:
    * Failed items – This report can be imported again to retry just the failed items.
    * Informational report – This report provides information for any fields that were set to use “default” values.
* Improve dynamic resizing for RDP sessions when tab window is expanded beyond original size (resizing session for larger windows/full screen).
* Added “About” screen to display version number, EULA and docs links.
* Added support for “Favorites”:
  * Favorites tab/page to view items that are marked as Favorites.
  * Launch connections from Favorites page.
  * Mark Local connections/Secrets/Folders as Favorites and add them to the Favorites page.
* Dark theme support for Mac and Windows (determined by OS).
* Improving validation for basic import/export file in JSON format.
* Added a back-off delay for Connection Manager login, which allows 3 attempts before adding a 5 second delay, increasing the delay by 5 seconds on each following attempt up to 25 second.
* Enforce Secret Server connections to use HTTPS (and not allowing HTTP).
* Added support for smart card passthrough for Secret Server based RDP connections.
* Additional options/settings for using Connection Manager as a protocol handler for Secret Server.
* Setting in CM to switch between using CM as SS protocol handler or SS as the protocol handler.
* Connection Manager build package will ship with Secret Server (to act as the SS Mac protocol handler).

## Bugs

* The size of the file download dialog is not correct (too small) when updating the application.
* Resolve CefSharp (CVE-2020-6418) vulnerability in web browser for Secret Server login.
* Fixing issue for launching Secrets that connect using RPD proxy.
