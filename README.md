# Introduction
Quick overview of sources and things to remind me of things to install

# Dual Boot Partitions
Separate partitions for OS and data so I can reimage without losing data. Well that was the plan until I made them too small to update so I had to reimage anyways.

Boot into Live USB with Linux. Install and create partitions using the tool.

Create GPT Drive.

1. EFI Boot partition; 512 MB; EFI
2. Linux Boot; ~40 GB; EXT4          (I had it at like 15 for Mint 21 and didn't have enough space to update to 22)
3. Linux Home; 35 GB; EXT4
4. Windows Boot; 75 GB; NTFS          (Requires 64 GB)
5. Shared Data; ---; ~~FAT~~ NTFS     (Many games and Proton will not launch when installed to a FAT partition. Mounting it with the method below still lets you read/write on Linux.)

Boot into USB and install Windows with a custom install. Use autoattend file if applicable. With GPT drive, make sure you boot with UEFI. With Ventoy, this is a separate option in the boot options (`UEFI: Generic` instead of `Generic` since it's a flash drive).

# [Scripts](https://github.com/Backup158/BashScripts)
Create `Scripts` folder in home directory (~/Scripts). Add snippet of code to `~/.bashrc` (make sure hidden files is enabled in Nemo, toggle with ctrl + h).
```
# Adds scripts folder to executable path
export PATH=$PATH:~/Scripts/
# Extends sudo to work with aliases
alias sudo='sudo '
```
Copy aliases into `~/.bash_aliases` from the Scripts repo.

## OBS Sinks
Creates a new null sink (for OBS only audio) and combined sink (OBS only + stream to headphones). Default sink is still the headphones. Route game audio through combined sink through pavucontrol (because I like GUIs). PulseAudio Volume Control, install through Mint's Software Manager. 

# Mount Partition with Steam Library
https://github.com/ValveSoftware/Proton/wiki/Using-a-NTFS-disk-with-Linux-and-Windows

Find partition name using `sudo fdisk -l` then `sudo blkid` for the UUID

Add to `/etc/fstab/`:        `/dev/nvme0n1p5 /mnt/data ntfs uid=1000,gid=1000,rw,user,exec,umask=000 0 0`. First entry is the name or UUID. ~~`vfat` is needed to be specified for FAT32~~ Don't use FAT

# App Settings
## Clock
Custom formatting in settings: `%a, %Y-%m-%d, %H:%M` to create something like `Mon, 2024-12-30, 14:21`
## Keyboard
Add custom shortcut to open gnome system monitor (task manager) to mimic Windows. Use `ctrl+shift+escape` to execute command `gnome-system-monitor`
## Celluloid
User Scripts: [Go to next file in folder with SHIFT + RIGHT_ARROW](https://github.com/jonniek/mpv-nextfile)
![celluloid](https://github.com/user-attachments/assets/2596439d-d5fc-4b2b-adc2-17e64496f75b)
## Media Info and mediainfo-gui
Shows video resolution and stuff. Install through Software Manager
