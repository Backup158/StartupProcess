# Introduction
Quick overview of sources and things to remind me of things to install.

The old README covers Mint and Bazzite. This version is for after I've switched to CachyOS. I didn't have any particular problems with Mint, but I wanted to try something more modern.

## Glossary

# Drive Partitioning
I separate my OS from my user data generally. I keep things in the home folder limited, so reimaging and updating was easier. Made it very easy to migrate from Mint to CachyOS.

Boot in with live Linux USB and keep the actual drive unmounted. Use disk management tools to resize and such.

| Name | Size | Format | Comments |
|---|---|---|---|
| Boot and Home | 128 GB | EXT4 | Your home drive will include all the dependencies and programs installed, especially Steam with its Proton prefixes. |
| Shared Data | The rest of the drive lol | BTRFS | Without dual booting, there's no need to mess with NTFS, especially with that being... iffy for Steam games. I'm trying out BTRFS since it's more modern and makes snapshots easier |


# [Scripts](https://github.com/Backup158/BashScripts)
Create `Scripts` folder in home directory (~/Scripts). Then add shortcuts, but I've been lazy.

# KDE Settings
## Region & Languages
**Time**: English (Sweden) `en_SE.UTF-8`

YYYY-MM-DD with a 24 hour clock.

## Wallpaper
Use [Waywallen](https://waywallen.github.io/) for slideshows. I think that makes it easier. This only works for the regular wallpaper itself though. Lock screen and login screen need to be static, since Waywallen needs to be running to show the wallpapers (make sure it's on startup). When you're not logged in, it can't be running.

# Installed Applications
## Vesktop
Install Vesktop for working stream audio and optimizations. Import settings from [repo](https://github.com/Backup158/VencordTheme/tree/main). Install Flatseal through MSM and give it permissions to access the memes folder.

## [OpenRGB](https://openrgb.org/)
Handles RGB for peripherals. Make sure it launches with startup.
