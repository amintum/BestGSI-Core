# BestGSI-Core
![Android Version](https://img.shields.io/badge/Android-16-3DDC84?style=for-the-badge&logo=android)
![Architecture](https://img.shields.io/badge/Architecture-arm64--ab-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Stable-success?style=for-the-badge)

BestGSI-Core is a highly debloated, custom Generic System Image (GSI) built for Project Treble compatible devices. 

This project is based on **RestlessOS** by Christopher A. Williamson [`cawilliamson`](https://github.com/cawilliamson/restlessos), which itself is a fork of **GrapheneOS** packaged as a GSI. BestGSI-Core takes that secure, privacy-respecting foundation and strips it down to the absolute bare essentials, giving you complete control over your device.

## ✨ Key Features

*   **Zero Bloatware:** We believe in user choice. BestGSI-Core comes with a strictly minimal app drawer. There are no pre-installed browser trackers, unwanted system tools, or forced services. You get a clean slate to download and install exactly what *you* want.
*   **Custom Default Wallpaper:** Unlike the upstream RestlessOS which boots to a pitch-black background, BestGSI-Core ships with a beautiful, pre-configured default wallpaper out of the box for a better first-boot experience.
*   **Dynamic System Update (DSU) Ready:** Fully compatible with Android's DSU feature. You can easily boot this image alongside your host OS for safe, seamless testing.
*   **Modern Android Base:** Built on Android 16 with Material You theming support.
*  Security update has date of January 5, 2027, to ensure smooth installation and **bypass rollback protections**. Actual patch is June 2026 same as restless.

## 📸 Screenshots

Here is a look at BestGSI-Core in action.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/6f7f630f-3198-48ea-b1b2-15cbbbf20c19" width="250" /><br>
      <b>Lock Screen</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/45f67742-fd0f-40d9-adb5-92e528982af0" width="250" /><br>
      <b>Home Screen</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/33845324-4310-4a54-be2c-a69f8b83b3d8" width="250" /><br>
      <b>Quick Settings</b>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/4cc85e41-a52b-4604-ad00-e468c9f1c3e3" width="250" /><br>
      <b>DSU Notification</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/2f7c0f15-7d9a-4dad-aa57-baf2cf0d4497" width="250" /><br>
      <b>App Drawer</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c25ebf63-e357-4fbc-80cd-68fbb3a88f14"" width="250" /><br>
      <b>System Information</b>
    </td>
  </tr>
</table>

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

**[Join the Telegram Support Group](https://t.me/amintumgsibuilds)**
