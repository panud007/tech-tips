# Batch Rename Files (Ganti Nama 100 File Sekaligus)

## 🔍 Masalah

Punya 100 foto liburan namanya `IMG_001.JPG`, `IMG_002.JPG`, dst.
Mau diganti jadi `Liburan_Bali_001.JPG`.
Kalau rename satu-satu... tangannya keriting. 😵

---

## ✅ Solusi 1: Windows Explorer (Bawaan)

1. Blok semua file (`Ctrl + A`).
2. Klik kanan file **pertama** -> **Rename**.
3. Ketik nama baru: `Liburan Bali (1).jpg`.
4. Enter.
5. Windows otomatis namain sisanya jadi `Liburan Bali (2).jpg`, dst.

*Kekurangan: Formatnya pasti pakai kurung ().*

---

## ✅ Solusi 2: PowerToys PowerRename (Pro Level) 💪

Aplikasi wajib dari Microsoft buat power user. [Download PowerToys](https://learn.microsoft.com/en-us/windows/powertoys/).

1. Blok file yang mau direname.
2. Klik kanan -> **PowerRename**.
3. Muncul menu canggih:
   - **Search for**: `IMG_` (Cari teks apa)
   - **Replace with**: `Bali_` (Ganti jadi apa)
   - Bisa pakai **Regex** buat pola rumit.
   - Bisa ubah huruf besar/kecil (Case sensitive).
4. Lihat preview di kanan. Kalau oke, klik **Apply**.

---

**Tags**: #lifehacks #productivity #rename #files #powertoys
**Level**: 🟢 Easy
