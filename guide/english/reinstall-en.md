<img align="right" src="https://raw.githubusercontent.com/Xhdsos/Port-Windows-POCO-F5-RN12T/main/marble.png" width="425" alt="Windows 11 Running On A Poco F5">


# Running Windows on the Poco F5

## Reinstallation
If you don't like your Windows version or you've bricked your Windows install, or anything else, you would probably just reinstall Windows. Thankfully this process is very easy.

> [!IMPORTANT]
> Quite obviously, this will erase all of your Windows files. If you'd like to back up any of them, you can do so by mounting Windows using the [WOA Helper](https://github.com/Xhdsos/Port-Windows-POCO-F5-RN12T/releases/download/Files/BETAwoahelper1.8.4.10.apk) app and manually copying any files you wish to keep


### Prerequisites

- ```Existing Windows and boot partitions``` (*If not met, [go back and just pretend this guide never existed](/guide/English/1-partition-en.md)*)

- [```Recovery Image```](https://github.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/releases/download/1.0/recovery.img)

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)


### Boot recovery to format the Windows and boot partitions

```cmd
fastboot boot <recovery.img>
```

### Format the partitions
> If it asks you to run it once again, do so
```cmd
adb shell format
```
## [Next step: Reinstalling Windows](/guide/English/3-install-en.md#Execute-msc)
