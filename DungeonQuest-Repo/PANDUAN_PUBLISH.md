# 🚀 Panduan Publish ke GitHub

Kamu **tidak perlu** menginstal Android Studio, Java, atau Node.js. GitHub yang membuat APK dan EXE otomatis.

## 1. Buat repository
1. Login ke [github.com](https://github.com), klik **New repository**.
2. Nama contoh: `dungeon-quest`. Pilih **Public**. Klik **Create repository**.

## 2. Upload semua file
Di halaman repo baru, klik **uploading an existing file**, lalu seret **seluruh isi folder ini** (folder `game`, `app-android`, `app-windows`, `.github`, `README.md`, dst).

> ⚠️ Pastikan folder `.github` ikut ter-upload (folder tersembunyi). Kalau lewat web susah, pakai **GitHub Desktop** atau git:
> ```
> git init
> git add .
> git commit -m "Dungeon Quest v1.0.0"
> git branch -M main
> git remote add origin https://github.com/USERNAME/REPO.git
> git push -u origin main
> ```

## 3. Ganti `USERNAME/REPO` di README
Buka `README.md`, ganti semua `USERNAME/REPO` dengan nama akun dan repo kamu (contoh: `budi/dungeon-quest`).

## 4. Izinkan Actions menulis Release
**Settings → Actions → General → Workflow permissions → Read and write permissions → Save.**

## 5. Rilis!
Buat tag versi, lalu GitHub membangun semuanya (±10 menit):
```
git tag v1.0.0
git push origin v1.0.0
```
Atau lewat web: **Releases → Draft a new release → Choose a tag → ketik `v1.0.0` → Create new tag → Publish release**.

Cek progres di tab **Actions**. Setelah hijau ✅, file `DungeonQuest-Android.apk` dan `DungeonQuest-Windows.exe` muncul otomatis di tab **Releases**, dan link di README langsung berfungsi.

## Update game
Edit `game/index.html`, commit, lalu buat tag baru (`v1.0.1`, `v1.1.0`, dst).

## Catatan penting
- **Tanda tangan APK:** keystore (`app-android/dungeonquest.keystore`, password `dungeonquest`) ikut di repo supaya update bisa dipasang di atas versi lama. Cocok untuk game hobi. Untuk Google Play Store, buat keystore pribadi dan simpan sebagai GitHub Secret.
- **Windows SmartScreen** akan memberi peringatan selama EXE belum ditandatangani sertifikat berbayar. Ini normal, panduannya sudah ada di README.
- Ingin installer Windows (Setup) selain versi portable? Ubah target `portable` menjadi `nsis` di `app-windows/package.json`.
