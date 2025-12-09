# Mengatasi Disk Usage 100% & Laptop Lemot

## 🔍 Masalah

Laptop terasa sangat berat, buka aplikasi lama, sering *not responding*. Pas dicek di Task Manager (`Ctrl+Shift+Esc`), kolom **Disk** merah menyala menunjukkan **100%**, padahal tidak sedang copy file besar.

Ini penyakit umum Windows 10/11, terutama yang masih pakai **HDD (Hard Disk)** biasa, bukan SSD.

---

## ✅ Solusi

Lakukan langkah ini berurutan sampai terasa ringan.

## 🚀 Solusi Otomatis (1-Click)

Gunakan script ini untuk mematikan service SysMain & Telemetry otomatis:

- **[.bat] Download Optimize Windows Script** (dari repo `supportkit-script`)
  [Klik Disini untuk Download](https://github.com/panud007/supportkit-script/blob/main/optimize-windows.bat)

### 1. Disable SysMain (Superfetch)

SysMain memuat aplikasi yang sering dipakai ke RAM agar cepat, tapi sering bikin Disk 100% di HDD.

1. Buka **CMD** (Run as Administrator).
2. Ketik:

   ```cmd
   net stop SysMain
   sc config SysMain start= disabled
   ```

### 2. Disable Connected User Experiences

Service telemetry yang sering scanning background.

1. Di CMD Administrator, ketik:

   ```cmd
   net stop DiagTrack
   sc config DiagTrack start= disabled
   ```

### 3. Matikan Windows Search Indexing (Opsional)

Kalau jarang pakai fitur search file explorer.

1. Di CMD Administrator:

   ```cmd
   net stop WSearch
   sc config WSearch start= disabled
   ```

*(PENTING: Kalau step ini dilakukan, pencarian file di Windows jadi lambat, tapi performa sistem ngebut).*

### 4. Ganti ke SSD (Solusi Permanen) 💡

Kalau laptop masih pakai HDD, solusi software di atas cuma "obat pereda nyeri". Solusi sembuhnya adalah **Ganti HDD ke SSD**. Kecepatan SSD 10x lipat lebih cepat dan masalah Disk 100% pasti hilang.

---

## 💡 Penjelasan

Windows 10/11 didesain optimal untuk SSD. Indexing, update, dan telemetry berjalan simultan di background. HDD tua tidak sanggup menangani request baca/tulis sebanyak itu sekaligus, makanya antrian (queue) disk jadi penuh (100%).

---

## 🎥 Video Tutorial

- [Cara Mengatasi Disk Usage 100% Windows 10/11 - WinPoin](https://www.youtube.com/results?search_query=cara+mengatasi+disk+usage+100+windows+10)

---

**Tags**: #windows #performance #slow #disk100 #optimization
**Level**: 🟡 Intermediate

**Terakhir diupdate**: 2025-12-09
