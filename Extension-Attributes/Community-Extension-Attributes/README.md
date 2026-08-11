# Community Extension Attributes

## Overview

A library of **317 community-sourced Jamf Pro Extension Attribute templates** in XML format, covering security reporting, backup status, system information, antivirus, disk encryption, and more. Each XML contains the display name, category, data type, and the inventory script (macOS shell, and for some attributes a Windows VBScript variant).

---

## Categories

| Category | Templates |
|---|---|
| Security Reporting | 66 |
| Backup (CrashPlan, LiveBackup, Retrospect, …) | 39 |
| System Information | 22 |
| AntiVirus (Sophos, Symantec, ClamXav, …) | 16 |
| Server | 12 |
| Operating System | 10 |
| Serial Numbers | 9 |
| Power Management | 8 |
| Disk Encryption | 8 |
| Networking | 5 |
| Other (system state, user info, virtualization, updates, …) | 22 |
| Uncategorized | ~100 |

---

## How To Use

1. In Jamf Pro go to **Settings → Computer Management → Extension Attributes → New**
2. Copy the script from the XML's `<scriptContentsMac>` block into a new Extension Attribute (or use the display name, category, and data type from the XML fields)
3. Set the **data type** and **inventory display** section to match the XML values
4. Save — the attribute is collected at the next inventory update (`sudo jamf recon`)

---

## Important Notes

- **Placeholders:** several templates contain `EditFromTemplate_…` variables (service-account usernames, server names). These must be filled in before use — they are placeholders, not real values.
- **Vintage:** many templates date from earlier Casper/Jamf Pro eras and reference legacy products (Deep Freeze, CrashPlan PROe, Sophos 9, Office 2011). **Test on a current macOS release before deploying** — treat these as starting points, not production-ready code.
- Attribution belongs to the original community authors.
