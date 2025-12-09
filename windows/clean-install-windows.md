# Panduan Clean Install Windows 10/11

## 🔍 Masalah

Laptop lemot parah, kena virus bandel, sistem error terus-menerus, atau mau *downgrade/upgrade* OS yang bersih. Solusi paling ampuh adalah **Clean Install** (Install Ulang).

---

## ⚠️ Peringatan Keras

- ❌ **SEMUA DATA DI DRIVE C: AKAN HILANG**.
- Data di drive lain (D:, E:) biasanya aman, tapi **sangat disarankan backup semua data penting** ke hardisk eksternal/cloud untuk jaga-jaga.
- Pastikan ingat/catat **Product Key** Windows (biasanya auto-detect kalau laptop bawaan, tapi cek dulu).

---

## ✅ Solusi

### Tahap 1: Persiapan (Wajib!)

1. **Flashdisk**: Minimal 8GB, kosong (data di flashdisk bakal dihapus).
2. **Download ISO Windows**:
   - [Windows 10 Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10)
   - [Windows 11 Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows11)
3. **Driver**: Siapkan driver WiFi/VGA (download di web resmi laptop kamu), simpan di flashdisk lain/HP. *Jaga-jaga kalau setelah install WiFi tidak detect.*

### Tahap 2: Bikin Bootable USB

1. Colok Flashdisk.
2. Jalankan **Media Creation Tool** yang didownload.
3. Accept Terms -> Pilih **Create installation media (USB flash drive)**.
4. Pilih **USB flash drive** -> Next.
5. Tunggu proses download & burn selesai (bisa lama tergantung internet).

### Tahap 3: Masuk ke BIOS/Boot Menu

1. Restart laptop.
2. Saat layar mati/logo muncul, tekan tombol Boot Menu berkali-kali:
   - **Asus**: `Esc` atau `F2`
   - **Acer**: `F12`
   - **HP**: `F9`
   - **Lenovo**: `F12` atau tombol recovery kecil di samping.
   - **Dell**: `F12`
3. Pilih **USB Flashdisk** kamu dari daftar -> Enter.

### Tahap 4: Proses Instalasi

1. **Language/Time**: Pilih sesuai selera (Time: Indonesia biar jam pas). Next -> **Install Now**.
2. **Product Key**: Klik **"I don't have a product key"** (nanti aktif sendiri kalau connect internet, asal edisinya sama: Home/Pro).
3. **Edition**: Pilih edisi yang sama dengan lisensi kamu (biasanya **Windows 10/11 Home Single Language** untuk laptop resmi Indo).
4. **License**: Accept -> Next.
5. **Installation Type**: Pilih **Custom: Install Windows only (advanced)**.

### Tahap 5: Partisi (Hati-hati!) 🚨

Ini bagian paling krusial.

1. Kamu akan lihat daftar partisi (Drive 0 Partition 1, 2, dst).
2. **Cari Drive C:** (Lihat dari ukurannya).
3. **Delete** partisi C: dan partisi kecil-kecil sistem (System Reserved, Recovery) **SAMPAI JADI SATU** bernama **"Drive 0 Unallocated Space"**.
4. **JANGAN DELETE DRIVE D:** (Data kamu disitu!). Lihat ukurannya baik-baik.
5. Klik **Unallocated Space** -> Klik **Next**.
6. Windows akan otomatis membuat partisi baru dan mulai install.

Tunggu proses copy file dan restart. Cabut flashdisk saat restart pertama.

### Tahap 6: Setup Awal (OOBE)

1. Ikuti petunjuk di layar (Region, Keyboard layout, WiFi).
2. **Windows 11 Wajib Internet**: Kalau mau bypass login akun Microsoft:
   - Di layar "Let's connect you to a network", tekan `Shift + F10`.
   - Ketik `OOBE\BYPASSNRO` -> Enter.
   - Laptop restart, nanti ada pilihan "I don't have internet".

---

## 💡 Tips Setelah Install

1. Connect WiFi -> **Windows Update**. Biarkan dia cari driver otomatis.
2. Install Driver VGA (Nvidia/AMD/Intel) terbaru.
3. Install aplikasi penting (Chrome, Office, dll).

---

## 🎥 Video Tutorial

Untuk yang visual learner, bisa tonton tutorial langkah demi langkah ini:

- [Cara Install Ulang Windows 11 Lengkap - LevelUp ID](https://www.youtube.com/results?search_query=cara+install+ulang+windows+11+pemula+levelup+id)
- [Cara Install Windows 10/11 Step by Step - GadgetIn](https://www.youtube.com/results?search_query=cara+install+windows+10+gadgetin)

> Pilih video terbaru untuk tampilan yang paling update.

---

## 🔗 Referensi

- [Cara Clean Install Windows 10 (Microsoft)](https://answers.microsoft.com/en-us/insider/forum/all/how-to-perform-a-clean-install-or-reinstall-of/aef0ae63-2117-41ee-a8ea-4a3181625b08)

---

**Tags**: #windows #install-ulang #clean-install #bootable #troubleshooting
**Level**: 🔴 Advanced

**Terakhir diupdate**: 2025-12-09
