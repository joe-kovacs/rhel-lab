# RHEL Installation

## Target

- Red Hat Enterprise Linux 10.2
- Architecture: x86_64
- Installation type: Physical dual boot with Debian
- Boot mode: UEFI
- Installer media: USB

## Installation Image

Downloaded image:

`rhel-10.2-x86_64-boot.iso`

Image size:

`994 MB`

SHA-256:

`675001a587c15f0c56c09beca6b1576c3be63cc4a0754e375ce93a6afda3dc8a`

The locally calculated SHA-256 checksum matched the checksum published
by Red Hat.

## USB Installation Media

USB device used during creation:

`/dev/sda`

Capacity:

`7.5 GB`

The existing Debian installation media on the USB drive was replaced
with the RHEL 10.2 Boot ISO.

The image was written with:

`sudo dd if=rhel-10.2-x86_64-boot.iso of=/dev/sda bs=4M status=progress conv=fsync`

After writing the image, the USB was verified with `lsblk`.

Detected label:

`RHEL-10-2-BaseOS-x86_64`

Anaconda boot partition was also detected.

## Current Status

- RHEL 10.2 ISO downloaded
- SHA-256 verified
- Bootable USB created
- Original Debian installation remains unchanged
- No disk partitions have been modified

## Next Step

Boot the Lenovo from the RHEL USB and perform a hardware compatibility
test before modifying the Debian partition.

Hardware to test:

- AMD Radeon 680M graphics
- Realtek RTL8852BE Wi-Fi
- Display
- Keyboard
- Touchpad
- Audio
- Network connectivity

Do not begin disk partitioning until the initial hardware test has
been completed.
