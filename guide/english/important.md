<img align="right" src="https://raw.githubusercontent.com/Xhdsos/Port-Windows-POCO-F5-RN12T/main/marble.png" width="425" alt="Windows 11 Running On A Poco F5">

# Running Windows on the Poco F5



## 24H2 EDL issues
If you ever create a restore point or modify any partitions (even on external devices) in disk manager in any 24H2 release, your device will be sent into EDL after rebooting. It's unknown what causes this issue, but it happens on any WoA device, not just the Poco F5.

If you want to use 24H2;
- **DO NOT CREATE A RESTORE POINT** or use software that creates one (like Driver Booster Pro).
- **DO NOT USE DISK MANAGER** to edit, create, format, or modify partitions in any way. This includes external devices.

## White line issues
In some extremely rare cases, your screen may display white lines after putting it to sleep in Windows. This is a hardware issue caused by Xiaomi shipping out screens with incompatible display configurations.

If you see white lines after sleeping in Windows, **REBOOT IMMEDIATELY!!**. These lines can become permanent if they stay on the screen for too long.

Currently the only solution is to either never put your device to sleep in Windows, or to sell your nabu and buy a new one.

























