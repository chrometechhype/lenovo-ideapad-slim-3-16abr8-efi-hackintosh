# 🇬🇧 EFI for Lenovo IdeaPad Slim 3 16ABR8

### macOS Sequoia • macOS Tahoe • macOS Big Sur

> 📌 This is the English version of the README
> 🇷🇺 Russian version: [README_RU.md](README_RU.MD)

---

## ⚠️ Important Notice

**The EFI for macOS Big Sur is completely different.**
This configuration is intended for **macOS Sequoia and Tahoe only**.
(Big Sur setup may share similarities, but requires a separate EFI.)

---

## 💻 Laptop Specifications

* **Model:** Lenovo IdeaPad Slim 3 16ABR8
* **CPU:** AMD Ryzen 7 7730U (Zen 2)
* **GPU:** AMD Radeon Vega 8
* **Audio:** Realtek ALC257
* **Camera:** Built-in
* **Wi-Fi / Bluetooth:** MediaTek MT7921 (not supported)
* **Bootloader:** OpenCore 1.0.5

### 🖥 Supported macOS

* macOS Sequoia (15.x)
* macOS Tahoe (26.x)

---

## 🧩 Included SSDTs

* SSDT-ALS0
* SSDT-Disable_Network_GPP4
* SSDT-EC
* SSDT-PLUG-ALT
* SSDT-PNLF
* SSDT-RMNE
* SSDT-USB-Reset
* SSDT-USBX
* SSDT-XOSI

---

## ✅ Working

* Full graphics acceleration (Vega 8)
* Audio *(limited, see notes below)*
* Built-in camera
* USB ports
* Smooth UI and animations
* Stable installation and boot

---

## ⚠️ Not Working

* ❌ Wi-Fi / Bluetooth (MediaTek MT7921 is not supported in macOS)

### 📌 Notes

* Internet is available via **USB tethering**
* HoRNDIS.kext is included in this EFI

---

## 🔊 Audio Status (Important)

* Audio works **only in early macOS Tahoe beta builds**
* Broken in newer versions (likely due to AppleHDA changes)
* Not yet fully fixed

---

## ⚙️ Boot Arguments

```
-v debug=0x100 keepsyms=1 npci=0x3000 -vi2c-force-polling alcid=11 revpatch=sbvmm amfi_get_out_of_my_way=1
```

---

## 📁 EFI Structure

```
EFI
├── BOOT
│   └── BOOTx64.efi
└── OC
    ├── ACPI
    ├── Drivers
    ├── Kexts
    ├── Tools
    ├── config.plist
    └── OpenCore.efi
```

---

## ⚠️ Disclaimer

This EFI is provided for educational purposes only.
Use at your own risk. No guarantees of full compatibility.
