# linux-mint-installation-case-study
A real-world Linux troubleshooting journey covering EFI, GRUB, Secure Boot, MOK errors, and Linux Mint installation issues on an old Dell laptop.

## Goal

Install Linux Mint 22.3 Cinnamon on a Dell Inspiron 3505 by replacing Windows 11.

## Hardware

- Laptop: Dell Inspiron 3505
- CPU: AMD Ryzen 5 3450U
- RAM: 8 GB
- SSD: SK hynix 256 GB NVMe
- HDD: 1 TB

## Symptoms

- Linux Mint installer crashed during "Copying files"
- Failed to start MokManager
- EFI/boot related issues
- Failed to import MOK state (`import_mok_state() failed`)

## Troubleshooting Steps

1. Recreated the bootable USB using Rufus.
2. Verified BIOS and Secure Boot settings.
3. Investigated EFI boot entries.
4. Reset BIOS defaults (F9).
5. Checked Linux Mint compatibility mode.
6. Investigated `mmx64.efi` and `grubx64.efi` boot files.
7. Collected logs instead of relying on guesses.

## Lessons Learned

- Read exact error messages.
- Verify before applying fixes.
- Use logs to find the root cause.
- BIOS, EFI and bootloader configuration are closely related.

## Status

🟡 In Progress

The installer still crashes during "Copying files". Further investigation will be done using installer logs.