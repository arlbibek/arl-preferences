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

1. ON CMD enter following command:

`slmgr.vbs -upk`    # To Remove product key

`slmgr /upk`        # To Uninstall product key

`slmgr /cpky`       # To clear product key from registry

\# The End
