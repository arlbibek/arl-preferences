# Windows Product Key

## Remove activate windows watermark

1. Create `remove.bat` file with the following text
```
@echo off
taskkill /F /IM explorer.exe
explorer.exe
exit
```

2. Run 'remove.bat' and then Restart your pc
---

## Product Key

__ON CMD enter following command:__

\# To Remove product key
`slmgr.vbs -upk`      

\# To Uninstall product key
`slmgr /upk`        

\# To clear product key from registry
`slmgr /cpky`       

\# The End
