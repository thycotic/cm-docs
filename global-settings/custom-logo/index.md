[title]: # (Use a Custom Logo in the Connection Manager Interface)
[tags]: # (custom,logo,interface)
[priority]: # (400)

# Use a Custom Logo in the Connection Manager Interface

In Connection Manager version 1.6 and higher, you can substitute the default logo in the Connection Manager interface with your own company branded logo using either of the two procedures below.

## Manual Procedure

1. Create two versions of your logo image file in PNG format.

   * One sized to 250 x 50 pixels, named `logo.png`. This version is the full-sized logo that will appear in the main interface.

   * One sized to 100 x 50 pixels named `logo_collapsed.png`. This version is the collapsed logo that appear when the left navigation panel is collapsed

1. Store both image files in the following location (if you don’t have this folder structure already, you’ll need to create it):
`C:\ProgramData\Thycotic\Connection Manager\Resources\`

1. Assign all users permissions to read, execute, and list folder content from this location.

1. Restart Connection Manager.

## Command Line Procedure

Users with administrator privileges can also specify the location of custom logo files during installation by running the following command:

`Thycotic.ConnectionManager.WindowsInstaller /quiet RUNCM=runCM KEYS="-logo C:\install\logo.png -logocollapsed C:\install\logocollapsed.png"`
