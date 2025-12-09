# Mengatasi Windows Update Error / Stuck

## 🔍 Masalah

- Windows Update stuck di 0% atau angka tertentu berjam-jam.
- Muncul pesan error code aneh (0x8007... dsb) saat update.
- Setelah restart, update gagal dan "Undoing changes".

---

## ✅ Solusi

Reset komponen Windows Update. Ini akan menghapus file update yang *corrupt* dan download ulang yang fresh.

### Cara Cepat (CMD Script)

1. Buka Notepad, copy script di bawah ini.
2. Save as `fix_update.bat` (pilih All Files).
3. Klik kanan file tersebut > **Run as Administrator**.

```batch
net stop wuauserv
net stop cryptSvc
net stop bits
net stop msiserver
Ren C:\Windows\SoftwareDistribution SoftwareDistribution.old
Ren C:\Windows\System32\catroot2 catroot2.old
net start wuauserv
net start cryptSvc
net start bits
net start msiserver
pause
```

### Cara Manual

Kalau takut pakai script, ini langkah manualnya:

1. Buka **CMD** (Admin).
2. Stop service update: `net stop wuauserv` dan `net stop bits`.
3. Buka File Explorer, ke `C:\Windows\SoftwareDistribution`.
4. **Hapus semua isi folder** `DataStore` dan `Download` di dalamnya.
5. Kembali ke CMD, start lagi: `net start wuauserv` dan `net start bits`.
6. Coba Check for Updates lagi.

---

## 💡 Penjelasan

Folder `SoftwareDistribution` adalah tempat Windows menyimpan file mentahan update yang didownload. Seringkali file di sini *corrupt* karena koneksi putus atau mati lampu. Dengan merename/menghapus folder ini, Windows dipaksa membuat folder baru dan download ulang file yang sehat.

---

## 🎥 Video Tutorial

- [Cara Mengatasi Windows Update Error - TechTuth](https://www.youtube.com/results?search_query=fix+windows+update+stuck+indonesia)

---

**Tags**: #windows #update #error #fix #cmd
**Level**: 🟡 Intermediate

**Terakhir diupdate**: 2025-12-09
