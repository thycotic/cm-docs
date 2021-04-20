[title]: # (Command Line Arguments)
[tags]: # (cm,install)
[priority]: # (115)

# Command Line Arguments to Create a Secret Server Connection on Install

The following command line arguments can be used to install Connection Manager and create a connection to Secret Server when using the MSI file.

>**Important**: /quite mode installation works only with Administrative privileges. If the MSI is run with /quite under normal user context, nothing will happen.

## Web Connection Example

```cmd
Thycotic.ConnectionManager.WixInstaller.msi  /quiet RUNCM=runCM KEYS="-ssurl ""https://connmanagerss.thycotic.net/ss"" -ssname ""n e w s e r v e r"" -ssauth web"
```

## Local Connection Example

```cmd
Thycotic.ConnectionManager.WixInstaller.msi  /quiet RUNCM=runCM KEYS="-ssurl ""https://connmanagerss.thycotic.net/ss"" -ssname ""n e w s e r v e r"" -ssauth local"
```

>**Note**: you have to use double quotes inside the KEYS parameter because the value of the KEYS parameter is quoted itself.
