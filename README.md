<div align="center">

<img src="https://raw.githubusercontent.com/Athar5443/pterodactyl-nodejs-egg/main/A.gif" alt="AtharsTech Logo" width="160" />

# **AtharsTech Node.js Pterodactyl Egg**

**Sebuah Egg Pterodactyl yang dirancang superior untuk menjalankan segala jenis aplikasi Node.js dengan otomatisasi dan fleksibilitas penuh.**

</div>

<div align="center">

[![GitHub Stars](https://img.shields.io/github/stars/Athar5443/pterodactyl-nodejs-egg?style=for-the-badge&logo=github&color=FFC107&logoColor=white)](https://github.com/Athar5443/pterodactyl-nodejs-egg/stargazers)
[![Node Version](https://img.shields.io/badge/Node.js-18,_20,_22,_25-339933?style=for-the-badge&logo=nodedotjs)](https://nodejs.org/)
[![Docker Support](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker)](https://hub.docker.com/r/athars5443/pterodactyl-egg)

</div>

---

## 🤔 **Mengapa Memilih Egg Ini?**

Egg ini bukan sekadar egg Node.js biasa. Dibuat untuk developer yang menginginkan **efisiensi** dan **kontrol**. Lupakan proses setup manual yang membuang waktu. Dengan *AtharsTech Node.js Egg*, server Anda akan siap berjalan dalam hitungan menit, lengkap dengan otomatisasi cerdas.

---

## ✨ **Fitur Unggulan**

| Ikon | Fitur                      | Deskripsi Singkat                                                                                                |
| :--: | :------------------------- | :--------------------------------------------------------------------------------------------------------------- |
| `📦` | **Dukungan Multi-Versi** | Jalankan aplikasi pada Node.js versi `18`, `20`, `22`, `25`, atau `latest`.                                     |
| `🖼️` | **Varian Image Lengkap** | Pilih image `base`, `graphics` (dengan canvas), atau `playwright` (untuk automasi browser) sesuai kebutuhan proyek. |
| `🔄` | **Otomatisasi Cerdas** | `git pull`, `npm install`, dan `npm update` otomatis saat server dinyalakan.                                       |
| `⚙️` | **Konfigurasi Fleksibel** | Kustomisasi perintah startup, repositori Git, branch, dan lainnya dengan mudah melalui variabel.                |
| `🚀` | **Deployment Instan** | Clone repositori dan install dependensi secara otomatis pada instalasi pertama.                                  |

---

## 🔧 **Variabel Startup**

Kelola server Anda dengan mudah melalui tab **"Startup"** di Pterodactyl Panel.

| Variabel Lingkungan | Deskripsi                                                                      | Nilai Default     |
| :------------------ | :----------------------------------------------------------------------------- | :---------------- |
| `STARTUP_CMD`       | Perintah utama untuk menjalankan aplikasi Anda.                                | `node index.js`   |
| `AUTO_INSTALL`      | Atur ke `true` untuk `npm install` otomatis jika `node_modules` tidak ada.     | `true`            |
| `AUTO_UPDATE`       | Atur ke `true` untuk `git pull` & `npm update` otomatis sebelum server start.  | `false`           |
| `GIT_ADDRESS`       | URL repositori Git yang akan di-clone saat instalasi server (opsional).        | *(kosong)* |
| `GIT_BRANCH`        | Nama branch dari repositori Git yang akan digunakan (opsional).                | *(kosong)* |

---

## 🐳 **Daftar Lengkap Docker Image**

Pilih image yang paling sesuai dengan kebutuhan aplikasi Anda dari daftar lengkap di bawah ini.

<details>
  <summary><strong>Klik untuk melihat semua Docker image yang tersedia</strong></summary>

  | Nama Image                                                 |
  | :--------------------------------------------------------- |
  | `athars5443/pterodactyl-egg:node18-base`                     |
  | `athars5443/pterodactyl-egg:node18-graphics`                 |
  | `athars5443/pterodactyl-egg:node18-playwright`               |
  | `athars5443/pterodactyl-egg:node18-playwright-full`          |
  | `athars5443/pterodactyl-egg:node18-full`                     |
  | `athars5443/pterodactyl-egg:node20-base`                     |
  | `athars5443/pterodactyl-egg:node20-graphics`                 |
  | `athars5443/pterodactyl-egg:node20-playwright`               |
  | `athars5443/pterodactyl-egg:node20-playwright-full`          |
  | `athars5443/pterodactyl-egg:node20-full`                     |
  | `athars5443/pterodactyl-egg:node22-base`                     |
  | `athars5443/pterodactyl-egg:node22-graphics`                 |
  | `athars5443/pterodactyl-egg:node22-playwright`               |
  | `athars5443/pterodactyl-egg:node22-playwright-full`          |
  | `athars5443/pterodactyl-egg:node22-full`                     |
  | `athars5443/pterodactyl-egg:node25-base`                     |
  | `athars5443/pterodactyl-egg:node25-graphics`                 |
  | `athars5443/pterodactyl-egg:node25-playwright`               |
  | `athars5443/pterodactyl-egg:node25-playwright-full`          |
  | `athars5443/pterodactyl-egg:node25-full`                     |
  | `athars5443/pterodactyl-egg:nodelatest-base`                 |
  | `athars5443/pterodactyl-egg:nodelatest-graphics`             |
  | `athars5443/pterodactyl-egg:nodelatest-playwright`           |
  | `athars5443/pterodactyl-egg:nodelatest-playwright-full`      |
  | `athars5443/pterodactyl-egg:nodelatest-full`                 |

</details>

---

## 🚀 **Panduan Instalasi**

1.  **Unduh Egg**: Ambil file `nodejs-egg.json` dari [repositori ini](https://github.com/Athar5443/pterodactyl-nodejs-egg/).
2.  **Impor ke Panel**:
    -   Masuk ke Pterodactyl Panel Anda sebagai **Administrator**.
    -   Navigasi ke `Admin` -> `Nests`.
    -   Klik tombol `Import Egg` dan unggah file `nodejs-egg.json`.
    -   Pilih **Nest "Node.js"** sebagai tujuan impor.
3.  **Buat Server Baru**: Egg sudah siap! Buat server baru dan pilih **"AtharsTech Node.js"** dari daftar Egg yang tersedia.

---

##  hosting **Butuh Server Pterodactyl?**

Siap menjalankan proyek Anda tapi belum punya server? Kami menyediakan server Pterodactyl berkualitas tinggi yang sudah terkonfigurasi dan siap pakai dengan harga terjangkau.

-   **Performa Cepat & Stabil**
-   **Setup Instan**
-   **Dukungan Penuh**

Hubungi kami untuk konsultasi dan pemesanan sekarang juga!

<div align="center">
<a href="https://wa.me/6281909789118">
<img src="https://img.shields.io/badge/WhatsApp-Hubungi%20Kami-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="Hubungi via WhatsApp">
</a>
</div>

---

<div align="center">
  <p>Dibuat dan dikelola oleh <b>AtharsTech</b></p>
  <p>Untuk dukungan atau pertanyaan, silakan hubungi <a href="mailto:support@athars.tech">support@athars.tech</a>.</p>
</div>
