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
5. Shared Data; ---; FAT

Boot into USB and install Windows with a custom install. Use autoattend file if applicable. With GPT drive, make sure you boot with UEFI. With Ventoy, this is a separate option in the boot options (`UEFI: Generic` instead of `Generic` since it's a flash drive).

# Setup Scripts
https://github.com/Backup158/BashScripts

Create `Scripts` folder in home directory (~/Scripts)

# Mount Steam Library
https://github.com/ValveSoftware/Proton/wiki/Using-a-NTFS-disk-with-Linux-and-Windows

Find partition name using `sudo fdisk -l` then `sudo blkid` for the UUID

Add to `/etc/fstab/`:        `/dev/nvme0n1p5 /mnt/data vfat uid=1000,gid=1000,rw,user,exec,umask=000 0 0`. First entry is the name or UUID. `vfat` is needed to be specified for FAT32
 
