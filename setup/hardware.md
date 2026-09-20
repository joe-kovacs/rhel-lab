# RHEL Lab Hardware

## System

- Manufacturer: Lenovo
- Model: IdeaPad Slim 3 15ARP10
- Machine Type: 83K7
- Architecture: x86_64
- RAM: 16 GB

## Processor

- AMD Ryzen 7 7735HS with Radeon Graphics

## Graphics

- AMD Radeon 680M
- PCI device: AMD/ATI Rembrandt
- Integrated graphics

## Network

### Wireless

- Realtek RTL8852BE
- PCIe 802.11ax / Wi-Fi 6 Wireless Network Controller

## Storage

- Micron MTFDKCD1T0QGN-1BN1AABLA
- NVMe SSD
- Capacity: 953.87 GiB (approximately 1 TB)
- Partition table: GPT
- Boot mode: UEFI

## Current Operating System

Debian GNU/Linux is currently installed as the primary operating system.

RHEL is planned as a physical dual-boot installation.

## RHEL Installation Notes

Hardware compatibility should be verified before installation, with
particular attention to:

- Realtek RTL8852BE wireless networking
- AMD Radeon 680M graphics
- Suspend/resume and power management
- UEFI boot configuration
