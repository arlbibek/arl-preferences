# Remove Linux from Dual Boot on Windows 10

## After you delete you Linux Partition from Windows 10 do following things:

1. Open Command Prompt (CMD) (as Administrator)
3. Type following commands:

```
diskpart
list disk                       # list all harddrives on your pc
select disk 0                   # Select disk you want to select (in my case '0')
list volume                     # display your selected disk's partition info
select volume 2                 # select one where the Volume 'Info' is labled 'System' (in my case '2')
assign letter=z                 # assigh letter 'z' to the selected volume
exit                            # exit diskpart
```

4. [Optional] Go to 'This PC' using File Explorer, you shall see Local Disk (z:) mounted to you computer.

5. Agian: Open CMD as Administrator
6. Type following commands:

z:
dir                             # list all directories in the 'z'
cd EFI                          # this shall take you inside the 'EFI' directory
dir                             # list all directories inside the 'EFI'
rmdir /S kali-linux             # remove os files (in my case kali-linux)
                                <br>(Be Cautious! Do not to remove anything important.)

7. Restart your pc and you should boot into Windows.

## That is all.

Reference: YouTube

\# The End
