<div align="center">

<img src="https://raw.githubusercontent.com/Athar5443/pterodactyl-nodejs-egg/main/A.gif" alt="AtharsTech Logo" width="160" />

# **AtharsTech Node.js Pterodactyl Egg**

**Egg Pterodactyl kustom untuk Node.js, dibuat untuk developer yang butuh fleksibilitas dan otomatisasi penuh.**

</div>

<div align="center">

[![GitHub Stars](https://img.shields.io/github/stars/Athar5443/pterodactyl-nodejs-egg?style=for-the-badge&logo=github&color=FFC107&logoColor=white)](https://github.com/Athar5443/pterodactyl-nodejs-egg/stargazers)
[![License](https://img.shields.io/github/license/Athar5443/pterodactyl-nodejs-egg?style=for-the-badge&color=4CAF50)](https://github.com/Athar5443/pterodactyl-nodejs-egg/blob/main/LICENSE)
[![Repo](https://img.shields.io/badge/Docker-Kunjungi%20Repo-2496ED?style=for-the-badge&logo=docker)](https://hub.docker.com/r/athars5443/pterodactyl-egg)
[![Node Version](https://img.shields.io/badge/Node.js-18,20,22,25-339933?style=for-the-badge&logo=nodedotjs)](https://nodejs.org/)

</div>

---

## 🚀 **Fitur**

Egg ini dibuat untuk mempermudah hidup Anda. Fokus di kodingan, biar server yang urus sisanya.

| Ikon | Fitur                      | Deskripsi Singkat                                                              |
| :--: | :------------------------- | :----------------------------------------------------------------------------- |
| `🔄` | **Otomatisasi Bawaan** | Otomatis `git pull`, `npm install`, & `npm update` saat server start.        |
| `📦` | **Support Multi-Versi** | Siap untuk Node.js versi `18`, `20`, `22`, `25`, dan `latest`.                 |
| `🖼️` | **Banyak Pilihan Image** | Dari `base` yang ringan sampai `full` dengan Playwright & Java. Pilih sesukamu. |
| `⚙️` | **Startup Fleksibel** | Gampang atur command, repositori Git, dan branch langsung dari panel.        |
| `⚡` | **Setup Cepat via Git** | Cukup masukkan URL repo, egg ini akan otomatis clone & install dependensi.   |

---

## 🔧 **Variabel Startup**

Atur semua kebutuhan startup server Anda langsung dari tab **"Startup"** di Pterodactyl.

| Variabel Lingkungan | Deskripsi                                                                 | Nilai Default     |
| :------------------ | :------------------------------------------------------------------------ | :---------------- |
| `STARTUP_CMD`       | Perintah untuk menjalankan aplikasi (contoh: `npm start` atau `pm2 ...`). | `node index.js`   |
| `AUTO_INSTALL`      | `true` = Otomatis `npm install` jika `node_modules` tidak ada.            | `true`            |
| `AUTO_UPDATE`       | `true` = Otomatis `git pull` & `npm update` setiap server start.          | `false`           |
| `GIT_ADDRESS`       | URL repo Git yang ingin di-clone saat instalasi. (Kosongkan jika manual)  | *(kosong)* |
| `GIT_BRANCH`        | Nama branch dari repo Git. (Kosongkan untuk branch default)               | *(kosong)* |

---

## 📦 **Pilihan Varian Docker Image**

Pilih image yang paling pas buat proyekmu. Setiap varian sudah termasuk semua paket dari varian sebelumnya (contoh: `:graphics` sudah termasuk semua isi `:base`).

<br>

<details>
  <summary><strong>1. <code>:base</code> — Esensial</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Lingkungan Node.js standar dengan tools umum.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 500 MB</td>
    </tr>
    <tr>
      <td><strong>Cocok Untuk</strong></td>
      <td>Aplikasi web biasa, API backend, bot Discord/Telegram simpel.</td>
    </tr>
    <tr>
      <td><strong>NPM Global</strong></td>
      <td><code>npm</code>, <code>yarn</code>, <code>pnpm</code>, <code>pm2</code></td>
    </tr>
    <tr>
      <td><strong>Paket Kunci</strong></td>
      <td><code>bash</code>, <code>curl</code>, <code>wget</code>, <code>git</code>, <code>unzip</code>, <code>build-essential</code>, <code>htop</code>, <code>nano</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>2. <code>:graphics</code> — Grafis & Media</strong></summary>
  <br>
  <table>
    <tr>
      <td><strong>Deskripsi</strong></td>
      <td>Semua dari <code>:base</code> + support untuk media, rendering, dan <strong>canvas</strong>.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 650 MB</td>
    </tr>
    <tr>
      <td><strong>Cocok Untuk</strong></td>
      <td>Bot dengan fitur manipulasi gambar (mis: Welcomer), generator gambar, pemrosesan <code>ffmpeg</code>.</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci</strong></td>
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
      <td>Semua dari <code>:graphics</code> + library lengkap untuk <strong>automasi browser</strong>.</td>
    </tr>
    <tr>
      <td><strong>Ukuran</strong></td>
      <td>~ 950 MB</td>
    </tr>
    <tr>
      <td><strong>Cocok Untuk</strong></td>
      <td>Web scraping, auto-testing, generator screenshot, atau proyek yang butuh <code>puppeteer</code> / <code>playwright</code>.</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci</strong></td>
      <td><code>playwright</code>, <code>chromium</code>, <code>firefox-esr</code>, <code>webgl-mesa</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>4. <code>:playwright-full</code> — Build Tools</strong></summary>
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
      <td><strong>Cocok Untuk</strong></td>
      <td>Proyek yang butuh kompilasi C/C++ (mis: <code>sqlite3</code>, <code>node-sass</code>, <code>bcrypt</code>) dari source.</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci</strong></td>
      <td><code>python3</code>, <code>make</code>, <code>gcc</code>, <code>g++</code>, <code>clang</code>, <code>node-gyp</code>, <code>cmake</code>, <code>libsqlite3-dev</code>, <code>libssl-dev</code></td>
    </tr>
  </table>
</details>

<details>
  <summary><strong>5. <code>:full</code> — Super Lengkap (Termasuk Java)</strong></summary>
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
      <td><strong>Cocok Untuk</strong></td>
      <td>Proyek Node.js yang perlu interaksi dengan Java (mis: bot musik <code>lavalink</code>, atau menjalankan file <code>.jar</code>).</td>
    </tr>
    <tr>
      <td><strong>Paket Kunci</strong></td>
      <td><code>openjdk-17-jre-headless</code></td>
    </tr>
  </table>
</details>

---

## ⚙️ **Cara Instalasi**

1.  **Download Egg**: Ambil file `nodejs-egg.json` dari [repositori ini](https://github.com/Athar5443/pterodactyl-nodejs-egg/).
2.  **Impor ke Panel**:
    -   Login sebagai **Admin** di Pterodactyl Panel.
    -   Pergi ke `Admin` -> `Nests`.
    -   Klik `Import Egg` dan upload file `nodejs-egg.json`.
    -   Pilih **Nest "Node.js"** saat impor.
3.  **Buat Server**: Siap! Saat buat server baru, pilih **"AtharsTech Node.js"** dari daftar Egg.

---

## 🛒 **Butuh Server Pterodactyl?**

Lagi cari server Pterodactyl buat host proyekmu? Kami juga menyediakan server hosting yang sudah terkonfigurasi, cepat, dan stabil dengan harga terjangkau.

-   **Performa Cepat & Stabil**
-   **Setup Instan**
-   **Dukungan Penuh**

Hubungi kami untuk tanya-tanya atau langsung pesan!

<div align="center">
<a href="https://wa.me/6281909789118">
<img src="https://img.shields.io/badge/WhatsApp-Hubungi%20Kami-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="Hubungi via WhatsApp">
</a>
</div>

---

<div align="center">
  <p>Dibuat dan dikelola oleh <b>AtharsTech</b></p>
  <p>Ada masalah atau pertanyaan? Hubungi <a href="mailto:support@athars.tech">support@athars.tech</a>.</p>
</div>
