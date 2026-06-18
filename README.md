# Linux Mint EFI/MOK Troubleshooting - Dell Inspiron 3505

## Overview

This repository documents a real-world troubleshooting case involving Linux Mint boot failures caused by EFI/MOK related issues on a Dell Inspiron 3505.

The purpose of this repository is to document the investigation process, findings and lessons learned while diagnosing Linux boot problems.

---

## Goal

Install Linux Mint 22.3 Cinnamon on a Dell Inspiron 3505.

---

## Hardware

- Laptop: Dell Inspiron 3505
- CPU: AMD Ryzen 5 3450U
- RAM: 8 GB
- SSD: SK hynix 256 GB NVMe
- HDD: 1 TB
- Firmware: UEFI

---

## Symptoms

The following errors were encountered while attempting to boot Linux Mint:

- Failed to start MokManager
- `import_mok_state() failed`
- `mmx64.efi` related boot errors

Linux Mint was unable to boot correctly.

---

## Investigation Process

The following steps were performed:

1. Checked BIOS settings.
2. Verified Secure Boot configuration.
3. Recreated the Linux Mint bootable media.
4. Investigated EFI boot entries.
5. Reset BIOS defaults (F9).
6. Examined EFI boot files.

---

## Workaround

During troubleshooting, modifying the EFI boot file allowed Linux Mint to boot successfully.

Path:

```text
EFI/BOOT/
```

Change performed:

```text
grubx64.efi -> mmx64.efi
```

> Note:
>
> This was a hardware-specific workaround that worked on my Dell Inspiron 3505.
>
> This should not be considered a universal solution for every Linux Mint installation.

---

## Lessons Learned

- Always read the exact error message.
- Avoid changing multiple BIOS settings at once.
- Verify information before applying fixes.
- Investigate EFI boot files before assuming hardware failure.
- Troubleshoot step by step instead of guessing.

---

## Disclaimer

This repository documents my personal troubleshooting experience.

Hardware, firmware versions and Linux distributions may behave differently on other systems.

Use the information for educational purposes and verify changes before applying them to your own device.

---

## Status

✅ EFI/MOK boot issue resolved.