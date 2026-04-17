🇬🇧 README — EFI for Lenovo IdeaPad Slim 3 16ABR8 (macOS Tahoe, macOS BigSur and macOS Sequioa)

> 📌 This is the English version of the README.

>🇷🇺 Русская версия доступна здесь: [README_RU.md](README_RU.MD)
[WARNING!] FOR BIG SUR, THE EFI IS COMPLETELY DIFFERENT! THIS INFORMATION APPLIES ONLY TO SEQUOIA AND TAHOE! (FOR BIG SUR, MOST THINGS ARE SIMILAR)

---

💻 Laptop specifications:

Model: Lenovo IdeaPad Slim 3 16ABR8

CPU: AMD Ryzen 7 7730U (Zen 2)

Graphics: AMD Radeon Vega 8

Audio: Realtek ALC257 ✅

Camera: Built-in ✅

Wi-Fi / Bluetooth: MediaTek MT7921 ❌

Bootloader: OpenCore 1.0.5

Supported macOS: macOS Sequioa (15.x) macOS Tahoe (26.x)



---

🧩 Included SSDTs:

SSDT-ALS0

SSDT-Disable_Network_GPP4

SSDT-EC

SSDT-PLUG-ALT

SSDT-PNLF

SSDT-RMNE

SSDT-USB-Reset

SSDT-USBX

SSDT-XOSI



---

✅ What works:

Full hardware graphics acceleration (Vega 8)

Audio (via alcid=11)

Built-in camera

USB ports 

Smooth interface and animations

Stable installation and boot process



---

⚠️ What does not work:

❌ Wi-Fi and Bluetooth are not supported — MediaTek MT7921 is not macOS-compatible

Notes: Internet access is available only via USB tethering from a phone
The required HoRNDIS.kext is already included in this EFI


---

⚙️ Boot arguments (NVRAM boot-args):
```
-v debug=0x100 keepsyms=1 npci=0x3000 -vi2c-force-polling alcid=11 revpatch=sbvmm amfi_get_out_of_my_way=1
```

---

📁 EFI structure:
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
