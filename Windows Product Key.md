# Windows Product Key

## Remove activate windows watermark
>Note: This doesnot removes watermark permanently.

1. Create `remove.bat` file with the following text
```
@echo off
taskkill /F /IM explorer.exe
explorer.exe
exit
```

2. Run 'remove.bat' and then Restart your pc
---

## Remove Product Key

__ON CMD enter following command:__

\# Remove product key

`slmgr.vbs -upk`      

\# Uninstall product key

`slmgr /upk`        

\# Clear product key from registry

`slmgr /cpky`       

\# The End
