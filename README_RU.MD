🇷🇺 README — EFI для Lenovo IdeaPad Slim 3 16ABR8 (macOS Tahoe, macOS BigSur и macOS Sequioa)

> 📌 Это русская версия файла README.

>🇺🇲 English version is available here: [Readme.md](README.md)
[ВНИМАНИЕ!] : ДЛЯ БИГСЮР СОВСЕМ ДРУГОЙ ЕФИ! ЭТА ИНФОРМАЦИЯ ТОЛЬКО ДЛЯ СЕКВОИ И ТАХОИ! (У БИГСЮР ПОЧТИ ВСЕ ТОЖЕ САМОЕ) 

---

💻 Основные характеристики ноутбука:

Модель: Lenovo IdeaPad Slim 3 16ABR8

Процессор: AMD Ryzen 7 7730U (Zen 2)

Графика: AMD Radeon Vega 8

Аудио: Realtek ALC257 ✅

Камера: Встроенная ✅

Wi-Fi / Bluetooth: MediaTek MT7921 ❌

Загрузчик: OpenCore 1.0.5

Поддерживаемая версия macOS: macOS Sequioa (15.x), macOS Tahoe (26.x)



---

🧩 Используемые SSDT:

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

✅ Что работает:

Аппаратное ускорение графики (Vega 8)

Аудио 

Встроенная камера

USB-порты

Анимации и интерфейс без ограничений

Установка и загрузка проходят стабильно



---

⚠️ Что не работает:

❌ Wi-Fi и Bluetooth не поддерживаются — чип MediaTek MT7921 несовместим с macOS

Заметка: Интернет возможен только через раздачу с телефона (USB-модем).
В состав EFI уже включён HoRNDIS.kext, необходимый для такой работы


---

⚙️ Аргументы загрузки (boot-args в NVRAM):
```
-v debug=0x100 keepsyms=1 npci=0x3000 -vi2c-force-polling alcid=11 revpatch=sbvmm amfi_get_out_of_my_way=1
```

---

📁 Структура EFI:
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
