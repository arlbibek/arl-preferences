# Add Open Wiindows Terminal Here Contex menu
## Step 01. Set the default directory in Windows Terminal. 
+ Open Windows Terminal, click on the drop-down button on the title bar and select "Settings". In the JSON file, add the below line to your default profile.

`"startingDirectory": "."

## Step 02. Create new Registry (reg) file (`wt.reg`) with following code.

```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\wt]
 @="Open Windows Terminal here"

[HKEY_CLASSES_ROOT\Directory\Background\shell\wt\command]
 @="C:\\Users\\<USER NAME>\\AppData\\Local\\Microsoft\\WindowsApps\\wt.exe"
```
> Note: Replace `<USER NAME>` with your Windows username

## Step 02. Save the file and double-click on it (`wt.reg`). You will be prompted whether you want to merge the reg file. Click on the "Yes" then the "Ok" button. 

## And [ Done ]