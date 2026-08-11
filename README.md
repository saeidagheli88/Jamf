# Jamf Pro Scripts & Extension Attributes

![Platform](https://img.shields.io/badge/platform-macOS-000000?logo=apple&logoColor=white)
![Shell](https://img.shields.io/badge/shell-zsh%20%7C%20bash-4EAA25?logo=gnubash&logoColor=white)
![Jamf Pro](https://img.shields.io/badge/Jamf-Pro-9BD3DD)
![License](https://img.shields.io/badge/license-MIT-2ea44f)

A collection of production-ready scripts and Extension Attributes for managing macOS devices with **Jamf Pro**. Each package lives in its own folder with full documentation and setup instructions; two community libraries provide ready-to-adapt templates.

---

## Categories

### 🧩 Extension Attributes
Custom inventory attributes collected at recon and shown on the computer record.

| Name | Description |
|---|---|
| [Apple-ID](./Extension-Attributes/Apple-ID/) | Reports which Apple ID (Apple Account) is signed in on the Mac — audit managed vs personal Apple ID usage |
| [MDE-NetExt-Status](./Extension-Attributes/MDE-NetExt-Status/) | Reports whether the Microsoft Defender for Endpoint Network Extension is installed and activated |
| [MDM-Communication-Status](./Extension-Attributes/MDM-Communication-Status/) | Flags Macs with broken MDM communication by scanning the system log for MDM identity errors |
| [Member-Of-AD-Group](./Extension-Attributes/Member-Of-AD-Group/) | Shows the logged-in user's AD group membership via Directory Service Attribute Mapping (no script needed) |

### 📜 Scripts
Deployed via Jamf Pro policies.

| Name | Description |
|---|---|
| [Install-Rosetta](./Scripts/Install-Rosetta/) | Silently installs Rosetta 2 on Apple Silicon Macs, with smart checks, retry logic, and full logging |
| [Rename-Device](./Scripts/Rename-Device/) | Renames the Mac to `Room-SerialNumber` using the Jamf Pro API (modern OAuth2 API Client & Role auth) |

### 🌐 Community Libraries
Community-sourced templates — fill in placeholders and test before deploying.

| Name | Contents |
|---|---|
| [Community-Scripts](./Scripts/Community-Scripts/) | 120+ community Jamf Pro scripts: AD/LDAP binding, security hardening, app installs/updates, AV tooling, networking, and more |
| [Community-Extension-Attributes](./Extension-Attributes/Community-Extension-Attributes/) | 317 Extension Attribute XML templates across security reporting, backup, system info, antivirus, encryption, and more |

---

## 📋 Conventions

- Own scripts are **zsh/bash**, run as root via Jamf Pro policies, and log their actions.
- Credentials are never hardcoded — API scripts take an **API Client ID/Secret via script parameters** (`$4`/`$5`) and read the Jamf Pro URL from the device's own management plist.
- Each package README documents configuration, Jamf Pro setup steps, and expected output.

---

## 👤 Author

Saeid Agheli — Intune & Jamf Administrator
https://github.com/saeidagheli88
