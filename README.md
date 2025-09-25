-----

# EkoxAutoBot-NTE

Bot Otomatis untuk berinteraksi dengan Ekox Testnet di jaringan Holesky. Skrip ini dirancang untuk melakukan aktivitas harian seperti Stake, Unstake, dan Claim secara otomatis untuk banyak wallet sekaligus.

## Fitur Utama

  - **Otomatisasi Aktivitas Harian**: Menjalankan fungsi Stake, Unstake, dan Claim secara berulang sesuai dengan konfigurasi yang Anda atur.
  - **Dukungan Multi-Wallet**: Mengelola dan menjalankan transaksi untuk semua *private key* yang Anda daftarkan di `pk.txt`.
  - **Dukungan Proxy**: Mendukung penggunaan proxy untuk setiap wallet untuk keamanan dan menghindari pembatasan.
  - **Konfigurasi Fleksibel**: Semua parameter (jumlah repetisi, rentang nominal, jeda waktu) dapat diubah melalui file `config.json` atau menu interaktif di dalam aplikasi.
  - **Antarmuka Terminal (CLI)**: Tampilan yang mudah digunakan untuk memantau log transaksi, status wallet, dan mengakses menu.

-----

## ✨ Fitur Baru: Auto Swap untuk Semua Wallet ✨

Untuk meningkatkan efisiensi, fitur "Auto Swap ETH & WETH" telah diperbarui secara signifikan:

  - **Tanpa Pilih Wallet Satu per Satu**: Anda tidak perlu lagi memilih setiap wallet secara manual untuk melakukan swap.
  - **Satu Kali Input Nominal**: Cukup masukkan jumlah ETH atau WETH yang ingin Anda swap satu kali.
  - **Eksekusi Massal**: Skrip akan secara otomatis menjalankan proses *wrap* (ETH ke WETH) atau *unwrap* (WETH ke ETH) untuk **semua wallet** yang terdaftar di `pk.txt` secara berurutan.

Fitur ini menghemat banyak waktu dan menyederhanakan proses manajemen likuiditas di semua akun Anda.

-----

## Cara Penggunaan

### 1\. Persyaratan

  - [Node.js](https://nodejs.org/) versi 18 atau lebih tinggi.
  - NPM (biasanya sudah terpasang bersama Node.js).

### 2\. Instalasi

1.  *Clone* atau unduh repositori ini ke komputer Anda.
2.  Buka terminal atau Command Prompt di dalam folder proyek.
3.  Jalankan perintah berikut untuk menginstal semua *dependency* yang dibutuhkan:
4.  ```bash
    git clone  https://github.com/Kyugito666/EkoxAutoBot-NTE
    cd EkoxAutoBot-NTE
    ```
    ```bash
    npm install
    ```

### 3\. Konfigurasi Wallet

1.  Buat file baru bernama `pk.txt` di dalam folder yang sama dengan `index.js`.

2.  Masukkan semua *private key* Anda ke dalam file `pk.txt`, di mana setiap kunci berada di baris baru.

    **Contoh isi `pk.txt`:**

    ```
    0xaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
    0xbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
    ```

### 4\. (Opsional) Konfigurasi Proxy

1.  Buat file baru bernama `proxy.txt`.
2.  Masukkan daftar proxy Anda, satu per baris. Format yang didukung adalah `http://user:pass@host:port` atau `socks5://user:pass@host:port`.
3.  Skrip akan secara otomatis mengaitkan setiap wallet dengan proxy yang sesuai urutannya.

### 5\. Menjalankan Bot

Gunakan perintah berikut di terminal untuk memulai bot:

```bash
npm start
```

Anda akan disambut dengan antarmuka menu di mana Anda bisa memulai aktivitas otomatis, melakukan swap, atau mengubah konfigurasi.

-----

## ⚠️ Penafian (Disclaimer)

**Gunakan skrip ini dengan risiko Anda sendiri.** Menyimpan *private key* dalam bentuk teks biasa memiliki risiko keamanan. Penulis skrip dan kontributor tidak bertanggung jawab atas kehilangan dana atau masalah apa pun yang mungkin timbul dari penggunaan bot ini. Selalu gunakan wallet yang didedikasikan untuk aktivitas semacam ini.

-----

## ©️ Hak Cipta dan Atribusi

Skrip ini pada dasarnya dibuat dan dikembangkan oleh **VinzSenzoo**. Semua kredit untuk fungsionalitas inti dan struktur awal diberikan kepadanya.

  - **Asal Skrip**: Komunitas NTExhaust
  - **Tutorial & Komunitas**: Anda bisa bergabung dengan komunitas dan mendapatkan tutorial lengkap melalui tautan Telegram [NTExhaust](https://t.me/NTExhaust).

Modifikasi pada skrip ini bertujuan untuk meningkatkan fungsionalitas dan efisiensi alur kerja.
