<div align="center">

<img src="https://raw.githubusercontent.com/Athar5443/pterodactyl-nodejs-egg/main/A.gif" alt="AtharsTech Logo" width="160" />

# **AtharsTech Node.js Pterodactyl Egg**

**Egg Pterodactyl paling komprehensif untuk developer Node.js yang menuntut stabilitas, kecepatan, dan kustomisasi tanpa kompromi.**

</div>

<div align="center">

[![GitHub Stars](https://img.shields.io/github/stars/Athar5443/pterodactyl-nodejs-egg?style=for-the-badge&logo=github&color=FFC107&logoColor=white)](https://github.com/Athar5443/pterodactyl-nodejs-egg/stargazers)
[![Repo](https://img.shields.io/badge/Docker-Kunjungi%20Repo-2496ED?style=for-the-badge&logo=docker)](https://hub.docker.com/r/athars5443/pterodactyl-egg)
[![Node Version](https://img.shields.io/badge/Node.js-18,20,22,25-339933?style=for-the-badge&logo=nodedotjs)](https://nodejs.org/)

</div>

---

## 🚀 **Fitur Utama**

Hemat waktu setup dan biarkan server Anda bekerja secara otomatis.

| Ikon | Fitur                      | Deskripsi Singkat                                                                                                |
| :--: | :------------------------- | :--------------------------------------------------------------------------------------------------------------- |
| `🔄` | **Otomatisasi Cerdas** | `git pull`, `npm install`, dan `npm update` otomatis saat server dinyalakan.                                       |
| `📦` | **Dukungan Multi-Versi** | Penuh dukungan untuk Node.js versi `18`, `20`, `22`, `25`, dan `latest`.                                        |
| `🖼️` | **Varian Image Lengkap** | Dari `base` minimalis hingga `full` dengan Playwright dan Java, pilih yang Anda butuhkan.                        |
| `⚙️` | **Konfigurasi Fleksibel** | Kustomisasi perintah startup, repositori Git, branch, dan lainnya dengan mudah melalui variabel.                |
| `⚡` | **Instalasi Cepat** | Clone repositori dan install dependensi secara otomatis pada instalasi pertama.                                  |

---

## 🔧 **Konfigurasi Variabel Startup**

Kelola server Anda dengan mudah melalui tab **"Startup"** di Pterodactyl Panel.

| Variabel Lingkungan | Deskripsi                                                                      | Nilai Default     |
| :------------------ | :----------------------------------------------------------------------------- | :---------------- |
| `STARTUP_CMD`       | Perintah utama untuk menjalankan aplikasi Anda.                                | `node index.js`   |
| `AUTO_INSTALL`      | Atur ke `true` untuk `npm install` otomatis jika `node_modules` tidak ada.     | `true`            |
| `AUTO_UPDATE`       | Atur ke `true` untuk `git pull` & `npm update` otomatis sebelum server start.  | `false`           |
| `GIT_ADDRESS`       | URL repositori Git yang akan di-clone saat instalasi server (opsional).        | *(kosong)* |
| `GIT_BRANCH`        | Nama branch dari repositori Git yang akan digunakan (opsional).                | *(kosong)* |

---

## 📦 **Analisis Varian Docker Image**

Pilih image yang paling sesuai untuk proyek Anda. Setiap varian **mewarisi** paket dari varian sebelumnya.

*(Contoh: `:graphics` sudah termasuk semua paket dari `:base`)*

<br>

<details>
  <summary><strong>1. <code>:base</code> — Lingkungan Dasar (Esensial)</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Lingkungan dasar Node.js dengan utilitas umum yang esensial.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 500 MB</td>
    </tr>
    <tr>
      <td><strong>Kasus Penggunaan</strong></td>
      <td>Aplikasi web standar, API backend, bot Discord/Telegram sederhana.</td>
    </tr>
    <tr>
      <td><strong>NPM Global</strong></td>
      <td><code>npm</code>, <code>yarn</code>, <code>pnpm</code>, <code>pm2</code></td>
    </tr>
    <tr>
      <td><strong>Paket Kunci APT</strong></td>
      <td><code>bash</code>, <code>curl</code>, <code>wget</code>, <code>git</code>, <code>unzip</code>, <code>build-essential</code>, <code>htop</code>, <code>nano</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>2. <code>:graphics</code> — Dukungan Grafis & Media</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Semua dari <code>:base</code> + dukungan untuk media, rendering, dan <strong>canvas</strong>.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 650 MB</td>
    </tr>
    <tr>
      <td><strong>Kasus Penggunaan</strong></td>
      <td>Bot dengan fitur manipulasi gambar (mis: Welcomer), generator gambar, pemrosesan video <code>ffmpeg</code>.</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci APT</strong></td>
      <td><code>ffmpeg</code>, <code>imagemagick</code>, <code>libnss3</code>, <code>libgtk-3-0</code>, <code>libasound2</code>, <code>fonts-liberation</code>, <code>xvfb</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>3. <code>:playwright</code> — Automasi Browser</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Semua dari <code>:graphics</code> + library lengkap untuk <strong>browser automation</strong>.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 950 MB</td>
    </tr>
    <tr>
      <td><strong>Kasus Penggunaan</strong></td>
      <td>Web scraping, auto-testing, generator screenshot, aplikasi yang butuh <code>puppeteer</code> atau <code>playwright</code>.</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci APT</strong></td>
      <td><code>playwright</code>, <code>chromium</code>, <code>firefox-esr</code>, <code>webgl-mesa</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>4. <code>:playwright-full</code> — Toolchain Build</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Semua dari <code>:playwright</code> + toolchain lengkap untuk <strong>build native modules</strong> (<code>node-gyp</code>).</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 1.2 GB</td>
    </tr>
    <tr>
      <td><strong>Kasus Penggunaan</strong></td>
      <td>Aplikasi yang butuh kompilasi C/C++ (mis: <code>sqlite3</code>, <code>node-sass</code>, <code>bcrypt</code>) dari source.</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci APT</strong></td>
      <td><code>python3</code>, <code>make</code>, <code>gcc</code>, <code>g++</code>, <code>clang</code>, <code>node-gyp</code>, <code>cmake</code>, <code>libsqlite3-dev</code>, <code>libssl-dev</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>5. <code>:full</code> — Lengkap (Termasuk Java)</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Semua dari <code>:playwright-full</code> + <strong>Java Runtime Environment (JRE)</strong>.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 1.3 GB</td>
    </tr>
    <tr>
      <td><strong>Kasus Penggunaan</strong></td>
      <td>Aplikasi Node.js yang perlu menjalankan proses Java (mis: bot musik <code>lavalink</code>, interaksi dengan <code>.jar</code>).</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci APT</strong></td>
      <td><code>openjdk-17-jre-headless</code></td>
    </tr>
  </table>
</details>

---

## ⚙️ **Panduan Instalasi Cepat**

1.  **Unduh Egg**: Ambil file `nodejs-egg.json` dari [repositori ini](https://github.com/Athar5443/pterodactyl-nodejs-egg/).
2.  **Impor ke Panel**:
    -   Masuk ke Pterodactyl Panel Anda sebagai **Administrator**.
    -   Navigasi ke `Admin` -> `Nests`.
    -   Klik tombol `Import Egg` dan unggah file `nodejs-egg.json`.
    -   Pilih **Nest "Node.js"** sebagai tujuan impor.
3.  **Buat Server Baru**: Egg siap digunakan! Saat membuat server baru, pilih **"AtharsTech Node.js"** dari daftar Egg.

---

## 🛒 **Butuh Server Pterodactyl?**

Siap menjalankan proyek Anda tapi belum punya server? Kami menyediakan hosting Pterodactyl berkualitas tinggi yang sudah terkonfigurasi, aman, dan siap pakai dengan harga terjangkau.

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
  <p>Untuk dukungan teknis atau pertanyaan, silakan hubungi <a href="mailto:support@athars.tech">support@athars.tech</a>.</p>
</div>
