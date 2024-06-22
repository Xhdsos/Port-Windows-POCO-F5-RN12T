<img align="right" src="https://raw.githubusercontent.com/Xhdsos/Port-Windows-POCO-F5-RN12T/main/marble.png" width="425" alt="Windows 11 Running On A POCO F5 // Redmi Note 12 Turbo">

# Running Windows on the POCO F5/Redmi Note 12 Turbo

## Installation

### Prerequisites
- ```Unlocked bootloader```

-  ```Brain```
  
- [```Recovery Image```](https://github.com/Xhdsos/Port-Windows-POCO-F5-RN12T/releases/download/Files/modded-twrp.img)

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)

### Notes:
> [!Warning]
> All your data will be erased! Back up now if needed.
> 
> DO NOT REBOOT YOUR TABLET if you think you made a mistake, ask for help in the [Telegram chat](https://t.me/woa_marble_davinci)
>

### Partitioning your device and backup boot
> [!NOTE]
> Don't know how to start? Unzip the downloaded [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools), then open ```command prompt``` or `powershell` as administrator and run the following command, replacing `"path\to\platform-tools"` with the actual path of the platform tools folder
```cmd
cd "path\to\platform-tools"
```
> Use this window throughout the entire guide. Do not close it.

#### Boot the modded recovery
> Replace **path\to** with the actual path of the recovery image
```cmd
fastboot flash recovery path\to\modded-twrp.img
fastboot reboot recovery
```

### Partitioning your device
> Unmount all partitions via the mount menu on your phone 
> 
> Replace **$** with the amount of storage you want Windows to have (do not add GB, just write the number)
> 
> If it asks you to run it once again, do so
```sh
adb shell partition $
```

### Make a backup of your existing boot image
```cmd
adb shell "dd if=/dev/block/platform/soc/1d84000.ufshc/by-name/boot$(getprop ro.boot.slot_suffix) of=/tmp/normal_boot.img" && adb pull /tmp/normal_boot.img
```

#### Check if Android still starts
> Reboot to check if Android still works. If it doesn't boot, wipe all data in recovery and try again.

```cmd
adb reboot
```


### [Next step: Get Root](/guide/english/2-rootguide-en.md)
