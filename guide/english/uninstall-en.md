<img align="right" src="https://raw.githubusercontent.com/Xhdsos/Port-Windows-POCO-F5-RN12T/main/marble.png" width="425" alt="Windows 11 Running On A Xiaomi Pad 5">

# Running Windows on the POCO F5/Redmi Note 12 Turbo

## Uninstallation

### Why is this needed?

If you want to uninstall windows this is used instead of deleting partitions manually to avoid human error + writing a whole dedicated guide to just uninstalling.

If you want to relock your bootloader you'll need your partition table to be stock.

### Prerequisites

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)
  
- [```Recovery Image (OrangeFox)```](https://github.com/Ctapchuk/android_device_xiaomi_marble-OFRP/releases)

- [```Recovery Image (TWRP)```](https://sourceforge.net/projects/recovery-for-xiaomi-devices/files/marble/)

### Notes

> Replace ```<gpt_both0.bin>``` with the path to the gpt_both0.bin file.

## Restore GPT

```cmd
fastboot flash partition:0 <gpt_both0.bin>
```

> [!Warning]
> DO NOT REBOOT TO RECOVERY NOW.
## Flash stock rom via fastboot to avoid dead phone or EDL
