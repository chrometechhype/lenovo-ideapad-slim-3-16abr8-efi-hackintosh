# 🇷🇺 EFI для Lenovo IdeaPad Slim 3 16ABR8

### macOS Sequoia • macOS Tahoe • macOS Big Sur

> 📌 Это русская версия README

> 🇺🇸 English version: [README.md](README.md)

---

## ⚠️ Важная информация

**EFI для macOS Big Sur полностью отличается.**
Данная конфигурация предназначена только для **macOS Sequoia и Tahoe**.
(Для Big Sur используется отдельный EFI, несмотря на схожесть настроек.)

---

## 💻 Характеристики ноутбука

* **Модель:** Lenovo IdeaPad Slim 3 16ABR8
* **Процессор:** AMD Ryzen 7 7730U (Zen 2)
* **Графика:** AMD Radeon Vega 8
* **Аудио:** Realtek ALC257
* **Камера:** Встроенная
* **Wi-Fi / Bluetooth:** MediaTek MT7921 (не поддерживается)
* **Загрузчик:** OpenCore 1.0.5

### 🖥 Поддерживаемые версии macOS

* macOS Sequoia (15.x)
* macOS Tahoe (26.x)

---

## 🧩 Используемые SSDT

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

## ✅ Работает

* Аппаратное ускорение графики (Vega 8)
* Аудио *(с ограничениями, см. ниже)*
* Встроенная камера
* USB-порты
* Плавный интерфейс и анимации
* Стабильная установка и загрузка

---

## ⚠️ Не работает

* ❌ Wi-Fi / Bluetooth (MediaTek MT7921 не поддерживается в macOS)

### 📌 Примечание

* Интернет доступен через **USB-модем (раздача с телефона)**
* В EFI уже включён HoRNDIS.kext

---

## 🔊 Статус аудио (важно)

* Звук работает **только в ранних бета-версиях macOS Tahoe**
* В более новых версиях может не работать
* Причина — изменения в аудиосистеме macOS
* Окончательное решение пока отсутствует

---

## ⚙️ Аргументы загрузки (boot-args)

```
-v debug=0x100 keepsyms=1 npci=0x3000 -vi2c-force-polling alcid=11 revpatch=sbvmm amfi_get_out_of_my_way=1
```

---

## 📁 Структура EFI

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

## ⚠️ Отказ от ответственности

EFI предоставляется в ознакомительных целях.
Использование осуществляется на ваш риск. Полная совместимость не гарантируется.
