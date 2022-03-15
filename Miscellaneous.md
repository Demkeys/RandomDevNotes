
----
C# Events and Delegates
* Events (C# Programming Guide): https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/events/
* Delegates (C# Programming Guide): https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/delegates/
* Handling and Raising Events: https://docs.microsoft.com/en-us/dotnet/standard/events/
* Delegate Class: https://docs.microsoft.com/en-us/dotnet/api/system.delegate
* Delegates vs Events: https://docs.microsoft.com/en-us/dotnet/csharp/distinguish-delegates-events
----
Unity Coroutines
* Coroutines: https://docs.unity3d.com/Manual/Coroutines.html
* WaitForSeconds: https://docs.unity3d.com/ScriptReference/WaitForSeconds.html
* AsyncOperation: https://docs.unity3d.com/ScriptReference/AsyncOperation.html
----
glTF File Format:
* glTF 2.0 Spec: https://www.khronos.org/registry/glTF/specs/2.0/glTF-2.0.html
* glTF Overview repo: https://github.com/KhronosGroup/glTF
* glTF Tutorial repo: https://github.com/KhronosGroup/glTF-Tutorials
----
### Kernel and Driver
* Difference between Kernel and Driver: https://stackoverflow.com/questions/30953314/what-is-difference-between-kernel-and-driver
* User mode and Kernel mode: https://docs.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/user-mode-and-kernel-mode
----
### Powershell
* Calling methods from a .Net namespace in PS: Use [] for the namespace and class. Then use :: to call the method. For example, [System.Convert]::ToString().
----
### Unity Android Dev
* Can Android apps made for one Android version work on another Android version?
Read 'Application Forward Compatibility' section on this page: https://developer.android.com/guide/topics/manifest/uses-sdk-element.html
----
### Ubuntu Core for Raspberry Pi
To copy the Ubuntu Core image over to the SD card you have to use the dd command. This overwrites the filesystem present on the SD card. Because of this, the SD card may not be recognized as a storage device by your PC and/or Phone. To be able to use the SD card as a storage device again, follow these steps:
* Cannot SD card (via card reader) to PC and find device name using 'fdisk -l'. For this example, assume the name /dev/sdb1.
* Zero out the SD card using 'dd if=/dev/zero of=/dev/sdb1 bs=8192'.
* Create file system on device using 'mkfs.vfat /dev/sdb1'.
* Additional: Before creating the file system, if you want to create partitions you can use 'parted' to do that. Note that while this creates partition(s), it doesn't necessarily create a file system on the device, so you'll still need to do that separately.
After completing these steps, the device should show up as a storage device in your PC and/or Phone.
Some useful links:
* https://askubuntu.com/questions/929787/bricked-my-sd-card-while-using-dd
* https://askubuntu.com/questions/511467/how-can-i-completely-erase-all-data-on-a-micro-sd-card
* https://unix.stackexchange.com/questions/315063/mount-wrong-fs-type-bad-option-bad-superblock
* https://help.ubuntu.com/stable/ubuntu-help/hardware-cardreader.html.en

Some useful commands: dd, parted, fdisk, df, lsusb, mkfs (mkfs.ntfs, mkfs.vfat, etc.)

NOTES:
* If 'fdisk -l' doesn't show the card reader and SD card devices, it is possible that the card reader might not be connected properly, either due to a loose connection or improperly working ports. While this isn't always the case, it can sometimes be the case. Try reconnecting and then list the devices again.
----
