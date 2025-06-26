# 💻 Hackintosh EFI for Acer Aspire 3 A315-54K

I made this repo for anyone who doesn't want to waste their time ❤️

> ✅ **macOS Sequoia is fully working!**

![macOS Screenshot](MACOS.png)

---

## 🔍 Overview

This repository contains the **EFI folder** and configuration files to run **macOS** on the Acer Aspire 3 A315-54K using **OpenCore**.  
It includes all the necessary **kexts**, **drivers**, and a pre-configured `config.plist` for a smooth installation and boot experience. 🚀

---

## 🧩 Supported Hardware

| Component     | Model/Details                             | Status         |
|---------------|-------------------------------------------|----------------|
| 💼 **Model**     | Acer Aspire 3 A315-54K                   | ✅ Supported    |
| ⚙️ **CPU**       | Intel Core i3-8130U (8th Gen)            | ✅ Supported    |
| 🖥️ **GPU**       | Intel UHD Graphics 620                   | ✅ Supported    |
| 🧠 **RAM**       | 8GB DDR4                                 | ✅ Supported    |
| 💾 **Storage**   | SSD (50GB or more)                       | ✅ Supported    |
| 📡 **Wi-Fi**     | Qualcomm QCA9377                         | ❌ Not Working (use USB dongle) |
| 🔵 **Bluetooth** | Intel Dual Band Wireless-AC 8265         | ❌ Not Working (use USB dongle) |
| 🔊 **Audio**     | Realtek ALC255                           | ✅ Patched      |
| 👆 **Others**    | Touchpad, keyboard, webcam               | ✅ Supported    |

---

## ✨ Features

- 🍎 macOS Ventura up to **Sequoia** compatible
- 🧰 **OpenCore bootloader** with minimal patches
- 🔋 **CPU power management** & SSDT fixes
- 🪟🍏 **Dual Boot** with Windows and macOS
- 🔌 Native **USB** (XHCI) support
- 🎧 Patched **audio** (ALC255 codec)
- 🌐 Ethernet / external Wi-Fi dongle support
- 💽 **SSD / NVMe** fully supported
- 🌙 **Sleep/Wake** works
- 🔋 Battery status + brightness keys functional

---

## 🚫 What Doesn't Work

- ❌ **Wi-Fi** – internal QCA9377 unsupported, use USB dongle
- ❌ **Bluetooth** – use USB Bluetooth dongle
- ❌ **Microphone not working** — The microphone has been tested but is currently non-functional.
~~- ⚠️ **Hardware acceleration issue** – purple tint on external display (internal display works fine)~~  
✅ Fixed thanks to [BudDeuce](https://discord.com/users/910329683726459010), who recommended [BetterDisplay](https://github.com/waydabber/BetterDisplay) for fixing display problems and unlocking refresh rates on external monitors.  
Big thanks to *waydabber* for this great tool!

---

## 🛠 Installation

1. 📥 Create a macOS USB installer using standard OpenCore guide  
2. 📁 Replace the USB's `EFI` folder with this repo’s EFI  
3. ⚙️ Edit `config.plist` (especially SMBIOS info)  
4. 🚀 Boot from USB and install macOS  
5. 💾 After installation, copy EFI to your internal drive’s EFI partition

---

## ⚙️ Configuration Details

- Main config file: `EFI/OC/config.plist`  
- Use [ProperTree](https://github.com/corpnewt/ProperTree) or OpenCore Configurator to edit SMBIOS  
- Kexts: `EFI/OC/Kexts`  
- SSDTs & ACPI patches: `EFI/OC/ACPI`  
- Drivers: `EFI/OC/Drivers`

---

## 🧯 Troubleshooting

- 🖥️ Boot issues? Enable verbose mode with `-v`
- 🎧 No audio? Recheck codec and AppleALC version
- 📶 No Wi-Fi? Use external USB adapter
- 🌙 Sleep not working? May require SSDT/BIOS tweaks

---

## 🙌 Credits

- [OpenCore](https://dortania.github.io/OpenCore-Install-Guide/) – Bootloader & documentation  
- [Dortania](https://dortania.github.io/) – Hackintosh documentation  
- Kext developers: Lilu, VirtualSMC, WhateverGreen, AppleALC 🔧  
- [pxradise](https://slat.cc/paradiso) – (me 😎) For creating and maintaining this repo
- [BudDeuce](https://discord.com/users/910329683726459010) - aided in finalizing the EFI and display fixes
- [waydabber](https://github.com/waydabber/) - For creating BetterDisplay!
---

## ⚠️ Disclaimer

This EFI is provided **as-is**. Use it at your own risk.  
Make sure to **backup your data** before installation.  
Designed specifically for **Acer Aspire 3 A315-54K** or similar hardware.

---

## 🤝 Contributing

Found an issue or have a fix?  
Feel free to **open an issue** or **submit a pull request** ✅  
Test your changes before submitting 🧪
