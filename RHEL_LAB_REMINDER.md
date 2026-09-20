# RHEL Lab Reminder

**Version:** 1.0  
**Project:** Red Hat Enterprise Linux / RHCSA Lab  
**Machine:** Lenovo laptop  
**Current host OS:** Debian GNU/Linux

---

## Project Purpose

This project documents my Red Hat Enterprise Linux learning journey
and preparation for the RHCSA exam.

The lab is intentionally being built on physical hardware rather than
inside a virtual machine.

Main objectives:

- Learn RHEL system administration through hands-on practice
- Prepare systematically for the RHCSA exam
- Understand the commands instead of only copying them
- Document labs, problems, troubleshooting and solutions
- Maintain the project as a GitHub portfolio
- Commit and push meaningful progress regularly

---

## Working Method

Whenever working on RHEL:

1. Work through tasks step by step.
2. Explain what a command does before or while using it.
3. Prefer hands-on exercises over only reading theory.
4. Document important commands and concepts.
5. Save useful screenshots.
6. Document errors and their solutions.
7. Update this reminder when reaching an important milestone.
8. Commit meaningful progress to Git.
9. Push completed work to GitHub.
10. Keep this project separate from `security-lab`.

---

## Repository

Local Debian path:

`/home/joe/Projects/rhel-lab`

Repository structure:

- `setup/` — installation, hardware and dual-boot documentation
- `notes/` — RHEL/RHCSA study notes
- `labs/` — practical exercises
- `scripts/` — administration scripts
- `troubleshooting/` — problems and solutions
- `screenshots/installation/` — installation evidence
- `screenshots/labs/` — lab evidence
- `screenshots/troubleshooting/` — troubleshooting evidence

GitHub repository will be created after the initial documentation is ready.

---

## Current Machine

Lenovo laptop

- RAM: 16 GB
- Storage: approximately 1 TB NVMe SSD
- Current OS: Debian GNU/Linux
- Planned OS: Red Hat Enterprise Linux
- Installation type: physical dual boot
- Virtual machine: intentionally not used

---

## Current Disk Layout

Disk:

`/dev/nvme0n1` — 953.9 GB NVMe

Partitions:

### `/dev/nvme0n1p1`

- Size: 976 MB
- Filesystem: FAT32
- Mounted at: `/boot/efi`
- Purpose: EFI System Partition
- UUID: `51F9-0DB5`

### `/dev/nvme0n1p2`

- Size: 939.2 GB
- Filesystem: ext4
- Mounted at: `/`
- Purpose: Debian root filesystem
- UUID: `c822be06-7a97-4c32-bff6-b822b1f235d1`

### `/dev/nvme0n1p3`

- Size: 13.7 GB
- Filesystem: swap
- Purpose: Debian swap
- UUID: `7f509ead-67e0-4477-8fde-1b00e3ff8626`

---

## Important Safety Note

There is currently no unallocated space for RHEL.

The large Debian ext4 partition must eventually be reduced to create
free space for the RHEL installation.

DO NOT resize, delete, format or modify any partition until the disk
layout, filesystem usage and backup situation have been verified.

The Debian installation must remain functional.

---

## Planned RHEL Environment

Target:

- Red Hat Enterprise Linux 10
- Physical installation
- UEFI boot
- Dual boot with Debian
- GNOME desktop
- Wayland
- RHEL storage configuration suitable for learning administration and LVM

Exact partition sizes have not yet been finalized.

---

## RHCSA Study Areas

Planned areas include:

- Command-line administration
- Files and directories
- Users and groups
- Permissions and ownership
- DNF package management
- systemd
- systemctl
- journalctl
- Processes
- Storage
- Partitions
- LVM
- Filesystems
- Mounting
- Networking
- SSH
- firewalld
- SELinux
- Boot process
- Recovery
- Shell scripting
- Troubleshooting

---

## Current Progress

Completed:

- Created `/home/joe/Projects/rhel-lab`
- Created repository directory structure
- Created screenshot directories
- Created initial `README.md`
- Inspected the current NVMe layout with `lsblk`
- Confirmed Debian uses UEFI
- Confirmed Debian root is ext4
- Confirmed there is currently no free partition for RHEL
- Created this reminder file

Not completed yet:

- Git repository initialization
- GitHub repository creation
- Full disk usage inspection
- Hardware identification
- Graphics identification
- Backup verification
- Debian partition resize
- RHEL installer download
- RHEL installation
- Dual-boot configuration
- First RHEL boot

---

## Next Step

Do NOT start partitioning yet.

Next:

1. Initialize the local Git repository.
2. Create the GitHub `rhel-lab` repository.
3. Commit and push the initial project structure.
4. Continue hardware and disk inspection.
5. Plan the safe Debian partition resize.
6. Document the preparation under `setup/`.

---

## Resume Instruction

When resuming this project in a new conversation:

**Continue the RHEL/RHCSA lab from this reminder file. Work step by step and update the repository documentation as progress is made.**
