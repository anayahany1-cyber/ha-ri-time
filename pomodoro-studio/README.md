# ☕ Pomodoro Studio - Lofi Study & Ambient Focus Sanctuary

Aplikasi web **Pomodoro Studio** interaktif, estetik bergaya *Flocus / Lofi Study*, dirancang rapi menggunakan **HTML, Tailwind CSS, dan JavaScript (Vanilla JS)** murni tanpa dependensi eksternal.

---

## ✨ Fitur & Pembaruan Terkini

### 1. 🌐 Dukungan Penuh Bahasa (Bilingual: Indonesia & English)
- Bahasa awal aplikasi adalah **English**. Pilihan bahasa dapat diatur kapan saja di **Modal Pengaturan > Akun & Bahasa**:
  - 🇮🇩 **Bahasa Indonesia**
  - 🇬🇧 **English**
- Mengubah bahasa secara langsung memperbarui seluruh antarmuka (mode pewaktu, tombol kontrol, sapaan waktu dinamis, tanggal lokal, kutipan motivasi, daftar tugas, dan semua tab pengaturan).

### 2. ⏱️ Desain Jam Bersih di Tengah (Tanpa Lingkaran)
- Tampilan jam digital besar (*huge minimalist typography*) diletakkan **simetris di tengah layar** tanpa bingkai lingkaran yang mengganggu.
- Dilengkapi penanda mode aktif (*Fokus / Focus*, *Istirahat Singkat / Short Break*, *Istirahat Panjang / Long Break*) dan indikator siklus sesi.
- Semua elemen (Pin Tugas, Tab Mode, Angka Jam, dan Tombol Kontrol) berada dalam **satu garis tengah yang rapi dan simetris**.

### 3. 📌 Sistem Task Cerdas (Auto-Rotate on Complete)
- Input pin tugas fokus berada di tengah tepat di atas jam.
- Daftar tugas dimulai dalam keadaan kosong; tambahkan tugas sendiri dari ikon task di kiri bawah.
- **Logika Cerdas**: Ketika tugas yang sedang difokuskan dicentang selesai, aplikasi **langsung menggantinya secara otomatis dengan tugas berikutnya yang belum dicentang**.
- Akses modal checklist tugas tersedia melalui satu ikon task di kiri bawah untuk menambah, menghapus, atau memilih tugas utama.

### 4. 💬 Kutipan Elegan di Kanan Atas (Tanda Petik)
- Kutipan inspiratif ditempatkan di **pojok kanan atas layar**, dirancang tanpa gelembung/bubble agar teks tidak terpotong.
- Format penulisan kutipan alami menggunakan tanda petik `“ ... ”` dan nama penulis `— ...`.
- Klik kutipan untuk berganti kutipan baru secara instan, atau biarkan berganti otomatis setiap 50 detik.

### 5. 🏷️ Logo Pomodoro di Kiri Atas Layar
- Logo identitas Pomodoro Studio diletakkan rapi di **pojok kiri atas layar** dengan estetika lembut dan minimalis.

### 6. ⛶ Dock Navigasi dan Tombol Fullscreen
- Dock melayang kanan bawah memuat streak harian, beranda, timer fokus (ikon buku), pengaturan, jendela timer mengambang, dan fullscreen.
- Ikon api streak baru muncul setelah sesi fokus pertama selesai, dengan hitungan awal 1. Hitungan tersimpan berdasarkan hari sesi fokus yang selesai dan berlanjut pada hari kalender berturut-turut; jika melewatkan satu hari, sesi fokus berikutnya memulai streak dari 1 lagi.
- Statistik sesi fokus tetap hanya bertambah saat sesi fokus benar-benar selesai.
- Alarm bawaan menggunakan nada lembut Soft Focus Chime; pilihan suara lain tetap tersedia di pengaturan.
- Tombol jendela timer mengambang membuka mini-window Picture-in-Picture yang dapat tetap terlihat di atas aplikasi lain. Fitur ini memerlukan browser Chromium yang mendukung Document Picture-in-Picture (seperti Chrome atau Edge terbaru) dan aplikasi dibuka lewat `http://localhost:5500/` atau HTTPS, bukan lewat file HTML langsung.
- Ikon play juga berubah menjadi pause saat timer berjalan.

### 7. 🎧 Terhubung dengan Spotify Player Resmi
- **Drawer Audio** kini memiliki 2 tab:
  1. 🎧 **Pemutar Spotify**:
     - Embed player resmi Spotify yang responsif dan terintegrasi rapi.
     - *Preset Cepat Playlist Lofi*: Lofi Beats, Peaceful Piano, Deep Focus, Chill Lofi Study, dan Jazz Vibes.
     - *Input Link Kustom*: Masukkan link playlist, album, atau lagu Spotify favorit Anda sendiri.
  2. 🌧️ **Suara Alam (Ambience Synth)**:
     - 5 suara alam berbasis Web Audio API (Hujan, Hutan, Ombak, Api Unggun, Kafe).
     - **Dual Soundscape**: Anda bisa mendengarkan Spotify bersamaan dengan suara hujan atau api unggun!

### 8. 🖼️ 5 Wallpaper Asli & Tema Visual
- 5 Wallpaper sesuai gambar yang Anda berikan:
  1. **Lofi Sunset Room** — Kamar studio musik senja & kucing di atas speaker.
  2. **Fuji Twilight** — Gunung Fuji berbalut awan senja ungu mistis.
  3. **Cozy Balcony Night** — Balkon malam berbintang & tanaman hias.
  4. **Emerald Forest Path** — Jalan setapak hutan hijau teduh berberkas sinar mentari.
  5. **Autumn Sanctuary** — Kanopi hutan musim gugur keemasan.
- Dilengkapi slider pengatur *Blur* dan *Dimming Overlay* agar kontras timer selalu terjaga.

---

## 🚀 Cara Menjalankan Aplikasi

Aplikasi dapat langsung diakses melalui browser:

1. **Akses Server Lokal**:
   ```
   http://localhost:5500/
   ```

2. **Buka File Langsung**:
   ```
   C:\Users\ASUS\.gemini\antigravity-ide\scratch\pomodoro-studio\index.html
   ```

---

## 📂 Struktur File

```
pomodoro-studio/
├── assets/
│   └── wallpapers/
│       ├── autumn-canopy.jpg       # Foto user: Kanopi musim gugur jingga
│       ├── cozy-balcony-night.png   # Foto user: Balkon malam berbintang
│       ├── emerald-forest.png      # Foto user: Jalan setapak hutan hijau
│       ├── fuji-twilight.jpg       # Foto user: Gunung Fuji senja ungu
│       └── lofi-sunset-room.png    # Foto user: Kamar studio lofi senja & kucing
├── index.html                      # Layout terpusat, header kiri-kanan, dan drawer Spotify
├── style.css                       # Tipografi besar, glassmorphism, dan transisi
├── app.js                          # Logika bilingual i18n, task auto-rotation, Web Audio, dan Spotify
├── server.ps1                      # Server lokal statis ringan (PowerShell)
└── README.md                       # Dokumentasi lengkap
```
