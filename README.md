# Readme
**Be sure to use this on AsahiLinux environment. This is NOT installation script, see https://asahilinux.org**
You should build mesa if you cannot detect gpu.
Also, there is some prebuilt binaries in dir ./essential
## Cloning
```bash
git submodule init
git submodule update --recursive
```
### u-boot.macho regeneration (For customizing U-boot functionalities)

    cat ./essential.macho
    Your device's DTB would be on /boot folder.

```bash
cd /boot/dtb-$(uname -r)
```
in this directory, you can find dtbs. You can determine your devices' file by form of tXXXX-j<NUMBER>.dtb 
### u-boot.macho regeneration
    
    cat ./essential/m1n1.macho **YOUR DTB IN HERE** ./essential/u-boot-nodtb.bin > u-boot.macho
### U-Boot Installation (on macOS)
kmutil configure-boot -c u-boot.macho -v [STUB OS PATH]
### See Further
https://gitlab.freedesktop.org

