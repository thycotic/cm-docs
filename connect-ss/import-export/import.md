[title]: # (CSV Import)
[tags]: # (user)
[priority]: # (501)
# Import of CSV Files

Connection Manager allows the import of Connection Manager .JSON, CSV, and RDP files for local connections data. 

This example if for CSV file imports.

1. Right-click on __Local Connections__.
1. Select __Import__.

   ![import](images/import.png "Import menu options")
1. Select from the import options available based on your source file.

## Importing Local Connection Data

The following example shows what to expect when importing local connections via CSV file into your Connection Manager instance.

1. In the Step 1 of 2 of the Import process,
   1. select the file to import,
   1. specify the connection type, and
   1. select with Delimiters are used in the import file, the default is comma separated.

   ![import 2](images/import-2.png "Import dialog, step 1 of 2")
1. Click __Next__.

   ![import 3](images/import-3.png "Step 2 of 2, field mapping information")

   By default Connection Manager maps the data from the import file to field mappings for the local connection information. Any data not recognized/mapped is indicated as unmapped and duplicate mappings are highlighted red. These potential errors can be fixed prior to the import.
1. Click __Finish__.

   ![import 4](images/import-4.png "Import confirmation information")

   Connections are imported as local and information about import errors is displayed.
1. To further examine which information failed to import, click __View more...__.

   ![import 5](images/import-5.png "CSV containing the connection data that failed to import")

   Connection Manager saved the connection data that failed to import in a separate file. The data can be edited and the file can be used to retry the import for the remaining connections.
1. Back in the Connection Manager UI, click __OK__ to close the __Import completed__ modal.

Example of Step 2 of 2 modal showing errors:

![errors](images/errors.png "Errors listed on import modal")
