# 🤖 AOSP-Kernel-Lab: The OS Architect Room

![Build Status](https://img.shields.io/badge/AOSP-Building...-3DDC84?style=for-the-badge&logo=android)
![Kernel](https://img.shields.io/badge/Kernel-Linux%20Mainline-blue?style=for-the-badge&logo=linux)
![Platform](https://img.shields.io/badge/Target-ARM64%20%7C%20x86__64-orange?style=for-the-badge)

> **"Owning the OS, from Boot to App."** > Repository ini adalah makmal penyelidikan untuk memahami lapisan paling dalam sistem operasi Android (AOSP) dan Kernel Linux. Di sini kita belajar bagaimana "menghidupkan" perkakasan melalui perisian sistem.

---

## 🎯 Objektif Lab

1.  **Kompilasi Kernel:** Membina imej kernel `zImage` / `Image.gz-dtb` yang dioptimumkan.
2.  **OS Customization:** Mengubahsuai `init.rc`, membina *boot animation* tersuai, dan menguruskan `Device Tree (DTS/DTB)`.
3.  **System Engineering:** Belajar proses *flashing* imej (`fastboot flash system`) dan teknik *debugging* melalui `adb logcat` dan `dmesg`.

---

## 🛠️ Latihan 1: Membina Build Environment (WSL2)

Android memerlukan persekitaran Linux yang kuat. Ikuti langkah ini untuk menyediakan "Workstation" anda:

### 1. Keperluan Sistem (Prerequisites)
Pastikan anda mempunyai sekurang-kurangnya 16GB RAM dan 300GB ruang storan SSD untuk AOSP penuh.

### 2. Pemasangan Tool Utama
```bash
# Pasang Toolchain & Dependencies
sudo apt update && sudo apt install -y \
    git-core gnupg flex bison build-essential zip curl zlib1g-dev \
    gcc-multilib g++-multilib libc6-dev-i386 libncurses5-dev \
    x11proto-core-dev libx11-dev libgl1-mesa-dev libxml2-utils \
    xsltproc unzip fontconfig python3 openjdk-17-jdk

# Pasang Repo Tool (Google)
mkdir -p ~/bin
curl [https://storage.googleapis.com/git-repo-downloads/repo](https://storage.googleapis.com/git-repo-downloads/repo) > ~/bin/repo
chmod a+x ~/bin/repo
export PATH=~/bin:$PATH

🚀 Langkah Seterusnya (Next Steps)
 * [ ] Modding Boot Animation: Menggantikan fail /system/media/bootanimation.zip dengan hasil seni sendiri.
 * [ ] Kernel Tuning: Mengubah pemproses (CPU) Governor untuk prestasi atau bateri.
 * [ ] Device Tree Discovery: Belajar bagaimana kernel mengenali komponen hardware dari Ground-Zero-Semiconductor.
🔗 Ekosistem Mastery
 * The Engine: X-Platform-Artifacts
 * The Hardware: Embedded-Nano-Firmware
 * The Central: Mastery-Core-Central
Lead Engineer: shiftcrypto69
"Building the foundation of the digital world."

---
