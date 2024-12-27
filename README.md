# Introduction
Quick overview of sources and things to remind me of things to install

# Dual Boot Partitions

# Setup Scripts
https://github.com/Backup158/BashScripts

Create `Scripts` folder in home directory (~/Scripts)

# Mount Steam Library
https://github.com/ValveSoftware/Proton/wiki/Using-a-NTFS-disk-with-Linux-and-Windows

Add to `/etc/fstab/`:        `/dev/nvme0n1p5 /mnt/data vfat uid=1000,gid=1000,rw,user,exec,umask=000 0 0`
