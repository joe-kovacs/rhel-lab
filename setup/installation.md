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

## Installation Result

RHEL 10.2 was successfully installed on the physical Lenovo laptop.

### Hardware Compatibility

Initial hardware testing was successful:

- AMD Radeon 680M graphics: working
- GNOME graphical installer: working
- Wayland session: working
- Realtek RTL8852BE Wi-Fi: detected and working
- Network connectivity: working
- Keyboard: working
- Hungarian keyboard layout: configured
- Red Hat CDN access: working
- Red Hat registration: successful

### Software Environment

Base environment:

`Server with GUI`

Desktop:

- GNOME
- Wayland

User:

- `joe`
- Administrative privileges enabled
- Direct root account disabled

### Dual-Boot Storage Result

The existing Debian ext4 root partition was safely shrunk by the
RHEL Anaconda installer.

Final disk layout:

- `/dev/nvme0n1p1` — 976 MB FAT32 — EFI System Partition
- `/dev/nvme0n1p2` — 690.4 GB ext4 — Debian
- `/dev/nvme0n1p3` — 13.7 GB swap — original Debian swap
- `/dev/nvme0n1p4` — 2 GB XFS — RHEL `/boot`
- `/dev/nvme0n1p5` — 246.8 GB LVM physical volume — RHEL

RHEL LVM layout:

- `rhel_lenovodebian-root` — 70 GB XFS — `/`
- `rhel_lenovodebian-swap` — 6.7 GB swap
- `rhel_lenovodebian-home` — 170.1 GB XFS — `/home`

### Boot Loader

The RHEL GRUB boot menu successfully detected:

- Red Hat Enterprise Linux 10.2
- RHEL rescue environment
- Debian GNU/Linux
- Debian recovery entries
- UEFI firmware settings

RHEL 10.2 successfully completed its first boot.

Debian is visible in GRUB but still needs a post-resize boot test.

### RHEL Environment Setup

Completed after first boot:

- Git 2.52.0 installed
- Git user identity configured
- Dedicated RHEL ED25519 SSH key created
- RHEL SSH key added to GitHub
- GitHub SSH authentication verified
- `rhel-lab` repository cloned to `/home/joe/Projects/rhel-lab`

### Remaining Validation

Before considering the dual-boot installation fully validated:

1. Boot Debian from the RHEL GRUB menu.
2. Verify Debian starts normally after the ext4 resize.
3. Return to RHEL.
4. Continue post-install configuration and RHCSA labs.
