# ⚔️ Dungeon Quest

Game petualangan pixel-art. Tersedia untuk **Android** dan **Windows**. Gratis, tanpa instalasi rumit.

## 📱 Cara Pasang di Android

**Syarat:** Android 7.0 ke atas.

1. Buka link unduhan **DungeonQuest-Android.apk** di atas dari HP kamu, lalu tunggu selesai diunduh.
2. Buka file yang terunduh (lewat notifikasi atau aplikasi *File Saya / Files*).
3. Jika muncul peringatan **"Install unknown apps"**, tekan **Settings**, lalu aktifkan **Allow from this source** untuk browser kamu. Kembali, lalu tekan **Install**.
4. Jika muncul peringatan Google Play Protect, tekan **Install anyway / Tetap instal**. Peringatan ini muncul karena game belum ada di Play Store, bukan karena berbahaya.
5. Buka **Dungeon Quest** dari layar utama. Selesai! 🎮

**Kontrol:** joystick dan tombol di layar. Putar HP ke landscape untuk tampilan layar penuh.

> Mau update? Cukup pasang APK versi baru di atas yang lama. Data tidak hilang.

---

## 💻 Cara Pasang di Windows

**Syarat:** Windows 10 / 11 (64-bit).

1. Klik link unduhan **DungeonQuest-Windows.exe** di atas.
2. Letakkan file di folder mana saja (misal Desktop). **Tidak perlu instalasi.**
3. Klik dua kali file tersebut untuk bermain.
4. Jika muncul layar biru **"Windows protected your PC"**, klik **More info** lalu **Run anyway**. Peringatan ini normal untuk game indie yang belum punya sertifikat berbayar.
5. Selesai! 🎮

**Kontrol:** keyboard. `F11` = layar penuh, `Esc` / `P` = pause.

---

## ❓ Masalah Umum

| Masalah | Solusi |
|---|---|
| APK tidak bisa dibuka / "App not installed" | Hapus versi lama Dungeon Quest dulu, lalu pasang ulang. |
| Antivirus memblokir EXE di Windows | Tambahkan ke pengecualian, atau unduh ulang dari halaman Releases resmi. |
| Tidak ada suara | Sentuh/klik layar sekali, browser engine butuh interaksi pertama untuk memutar audio. |
| Layar Android terpotong | Putar HP ke landscape, atau geser dari tepi atas untuk menampilkan status bar. |

## 🛠️ Untuk Developer

Struktur proyek:

```
game/index.html      ← kode game (satu-satunya yang perlu kamu edit)
app-android/         ← pembungkus Android (Capacitor)
app-windows/         ← pembungkus Windows (Electron)
.github/workflows/   ← build otomatis APK + EXE
```

Panduan publish ke GitHub: lihat [`PANDUAN_PUBLISH.md`](PANDUAN_PUBLISH.md).

