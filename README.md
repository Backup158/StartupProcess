# Introduction
Quick overview of sources and things to remind me of things to install

## Glossary

# Drive Partitioning
I separate my OS from my user data generally. I keep things in the home folder limited, so reimaging and updating was easier. Made it very easy to migrate from Mint to CachyOS.

Boot in with live Linux USB and keep the actual drive unmounted. Use disk management tools to resize and such.

| Name | Size | Format | Comments |
|---|---|---|---|
| Boot and Home | 128 GB | EXT4 | Your home drive will include all the dependencies and programs installed, especially Steam with its Proton prefixes. |
| Shared Data | The rest of the drive lol | BTRFS | Without dual booting, there's no need to mess with NTFS, especially with that being... iffy for Steam games. I'm trying out BTRFS since it's more modern and makes snapshots easier |
