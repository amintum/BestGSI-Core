# BestGSI-Core

BestGSI-Core is a highly debloated, custom Generic System Image (GSI) built for Project Treble compatible devices. 

This project is based on **RestlessOS** by Christopher A. Williamson (`cawilliamson`), which itself is a fork of **GrapheneOS** packaged as a GSI. BestGSI-Core takes that secure, privacy-respecting foundation and strips it down to the absolute bare essentials, giving you complete control over your device.

## ✨ Key Features

*   **Zero Bloatware:** We believe in user choice. BestGSI-Core comes with a strictly minimal app drawer. There are no pre-installed browser trackers, unwanted system tools, or forced services. You get a clean slate to download and install exactly what *you* want.
*   **Custom Default Wallpaper:** Unlike the upstream RestlessOS which boots to a pitch-black background, BestGSI-Core ships with a beautiful, pre-configured default wallpaper out of the box for a better first-boot experience.
*   **Dynamic System Update (DSU) Ready:** Fully compatible with Android's DSU feature. You can easily boot this image alongside your host OS for safe, seamless testing.
*   **Modern Android Base:** Built on Android 16 with Material You theming support.

---

## 📸 Screenshots

Here is a look at BestGSI-Core in action.

### The Bloat-Free Promise
<img width="1080" height="2460" alt="Screenshot_20260721-061622" src="https://github.com/user-attachments/assets/2f7c0f15-7d9a-4dad-aa57-baf2cf0d4497" />

> **Clean App Drawer:** Proof of our bloat-free philosophy. The OS ships with only three essential system apps: **Droid-ify** (for open-source app downloads), **Files**, and **Settings**. The rest is entirely up to you.

### Custom Out-of-the-Box Experience
<img width="1080" height="2460" alt="Screenshot_20260721-061605" src="https://github.com/user-attachments/assets/6f7f630f-3198-48ea-b1b2-15cbbbf20c19" />
<img width="1080" height="2460" alt="Screenshot_20260721-061609" src="https://github.com/user-attachments/assets/45f67742-fd0f-40d9-adb5-92e528982af0" />

> **Home & Lock Screen:** Showcasing the custom default wallpaper included in the build—a vibrant, illustrated nature landscape featuring a lake, mountains, and a dock. This replaces the default black background and integrates perfectly with Android's Material You color extraction, tinting the system clock and UI elements in a matching soft green.

### DSU Compatibility & UI
<img width="1080" height="2460" alt="Screenshot_20260721-061618" src="https://github.com/user-attachments/assets/4cc85e41-a52b-4604-ad00-e468c9f1c3e3" />
<img width="1080" height="2460" alt="Screenshot_20260721-061627" src="https://github.com/user-attachments/assets/33845324-4310-4a54-be2c-a69f8b83b3d8" />

> **Quick Settings & DSU:** The notification panel showing an active "Dynamic System Updates" instance running on the "Amintum" Wi-Fi network. The expanded Quick Settings panel highlights the clean layout and the custom green Material You theming generated from the default wallpaper. 

### System Information
<img width="1080" height="2460" alt="Screenshot_20260721-061638" src="https://github.com/user-attachments/assets/c25ebf63-e357-4fbc-80cd-68fbb3a88f14" />

> **About Device:** Verifying the system details. BestGSI-Core runs on Android 16, utilizing the `BestGSI-Core-16.0.0-Amintum` build number, and features a patched security update date of January 5, 2027, to ensure smooth installation and bypass rollback protections.

---

## 🤝 Credits & Acknowledgments

*   **Christopher A. Williamson (`cawilliamson`):** For the incredible work on [RestlessOS](https://github.com/cawilliamson/restlessos) and the Treble patching logic.
*   **GrapheneOS:** The upstream foundation for this privacy and security-focused OS.

---

### Installation

Your device must have an unlocked bootloader.
You must disable AVB with vbmeta.
Then wipe and factory reset.

adb devices

adb reboot bootloader

fastboot flash vbmeta vbmeta.img --disable-verity --disable-verification

fastboot reboot fastboot

fastboot erase system

fastboot flash system GSI_File_Name.img

fastboot reboot recovery → Clear data/cache → Factory reset

Error: "out of space" when flashing, use: fastboot delete-logical-partition product

If the error persists, use: fastboot delete-logical-partition system fastboot create-logical-partition system 0

# 💬 Support & Community

Need help, want to report a bug, or just want to stay updated on the latest builds and patches? Join our official community!

## 🚀 Join Us on Telegram

Get direct support, share your feedback, and connect with other users flashing BestGSI Avintum:

**[Join the Telegram Support Group](https://t.me/amintumgsibuilds)**
