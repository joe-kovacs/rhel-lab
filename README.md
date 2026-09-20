# Red Hat Enterprise Linux Lab

Hands-on Red Hat Enterprise Linux system administration lab documenting
my RHCSA preparation, practical exercises, troubleshooting, and Linux
administration experience.

## Goals

- Install and configure Red Hat Enterprise Linux on physical hardware
- Prepare for the Red Hat Certified System Administrator (RHCSA) exam
- Build practical RHEL system administration experience
- Practice administration tasks from the command line
- Document problems, solutions, and lessons learned
- Build a reproducible Linux administration portfolio

## Lab Environment

### Hardware

- Lenovo laptop
- 1 TB NVMe SSD
- 16 GB RAM
- Physical installation (no virtual machine)

### Operating Systems

- Debian GNU/Linux — existing primary system
- Red Hat Enterprise Linux — planned dual-boot installation

### Current Disk Layout

| Device | Size | Filesystem | Purpose |
|---|---:|---|---|
| `/dev/nvme0n1p1` | 976 MB | FAT32 | EFI System Partition |
| `/dev/nvme0n1p2` | 939.2 GB | ext4 | Debian `/` |
| `/dev/nvme0n1p3` | 13.7 GB | swap | Swap |

The RHEL installation space will be created by safely shrinking the
existing Debian partition after verifying disk usage and partition layout.

## Repository Structure

- `setup/` — installation, hardware, dual-boot and initial configuration
- `notes/` — study notes and command references
- `labs/` — hands-on RHCSA/RHEL exercises
- `scripts/` — administration scripts
- `troubleshooting/` — problems, investigation and solutions
- `screenshots/installation/` — installation and dual-boot evidence
- `screenshots/labs/` — lab screenshots
- `screenshots/troubleshooting/` — troubleshooting evidence
- `RHEL_LAB_REMINDER.md` — current project status and next steps

## Topics

The lab will cover areas including:

- User and group management
- File permissions and ownership
- Package management with DNF
- systemd and service management
- Logging and journalctl
- Storage and LVM
- Filesystems and mounting
- Networking
- SSH
- firewalld
- SELinux
- Boot and recovery
- Shell administration
- Troubleshooting

## Current Status

**Phase 1 — RHEL installation preparation**

The existing Debian installation and NVMe disk layout are being
documented before making any partition changes.

No disk modifications have been performed yet.
