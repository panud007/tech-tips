# Cara Rollback Windows 11 ke Windows 10

## 🔍 Masalah

Sudah upgrade ke Windows 11 tapi merasa kurang cocok, lemot, atau ada aplikasi yang tidak support? Kamu bisa kembali (rollback) ke Windows 10.

Ada 2 skenario:

1. **Kurang dari 10 hari** sejak upgrade: Bisa pakai fitur "Go Back" (Mudah & Data Aman).
2. **Lebih dari 10 hari**: Opsinya "Go Back" hilang, harus Clean Install (Data di C: hilang).

---

## ✅ Solusi

### Skenario 1: Kurang dari 10 Hari (Fitur Go Back)

Ini cara paling aman karena file dan aplikasi kamu tetap terjaga (mayoritas).

1. Buka **Settings** (`Win + I`).
2. Masuk ke **System** > **Recovery**.
3. Di bagian **Recovery options**, cari "Go back".
4. Klik tombol **Go back**.
   - *Note: Kalau tombolnya abu-abu atau tidak ada, berarti sudah lewat 10 hari (lihat Skenario 2).*
5. Akan muncul window survey "Why are you going back?", pilih alasan apa saja (misal: "Windows 11 is not reliable"), lalu klik **Next**.
6. "Check for updates?" -> Klik **No, thanks**.
7. Baca warning "What you need to know" -> Klik **Next**.
8. "Don't get locked out" (ingat password lama kalau ada) -> Klik **Next**.
9. Klik **Go back to Windows 10**.

Komputer akan restart dan proses rollback dimulai. Tunggu sampai selesai (biasanya 15-30 menit).

### Skenario 2: Lebih dari 10 Hari (Clean Install)

⚠️ **PERINGATAN**: Cara ini akan menghapus semua data di drive C (System). **BACKUP DATA PENTING DULU!**

1. Download **Media Creation Tool Windows 10** dari website resmi Microsoft.
2. Jalankan tool-nya, pilih **Upgrade this PC now**.
3. Ikuti langkah-langkahnya.
4. Saat di bagian "Ready to install", pastikan pilihannya **Nothing** di bagian "Keep files and apps" (karena downgrade tidak bisa keep files kalau lewat 10 hari).
5. Lanjutkan proses install sampai selesai.

Alternatif lain: Buat Bootable USB Windows 10 pakai Rufus, lalu install ulang via bios.

---

## 💡 Penjelasan

Microsoft memberikan waktu "trial" 10 hari untuk user Windows 11. Selama masa ini, file system Windows 10 yang lama disimpan di folder `Windows.old` di drive C.

- Jika pakai fitur **Go Back**, sistem mengembalikan file dari `Windows.old`.
- Setelah 10 hari, Windows otomatis menghapus `Windows.old` untuk menghemat storage, makanya fitur Go Back hilang.

**Tips:** Kalau baru upgrade dan masih ragu, jangan hapus folder `Windows.old` lewat Disk Cleanup.

---

## ⚠️ Catatan Penting

- **Backup Data**: Selalu backup data penting sebelum melakukan perubahan sistem besar, meskipun pakai cara "Go Back".
- **Aplikasi**: Beberapa aplikasi yang diinstall *setelah* upgrade ke Windows 11 mungkin akan hilang saat rollback.
- **Laptop**: Pastikan charger tercolok selama proses.

---

## 🎥 Video Tutorial

- [Cara Downgrade Windows 11 ke 10 (Go Back) - Asani TV](https://www.youtube.com/results?search_query=cara+rollback+windows+11+ke+10+indonesia)
- [Cara Balik ke Windows 10 Tanpa Hilang Data - Handa](https://www.youtube.com/results?search_query=downgrade+windows+11+to+10+indonesia+no+data+loss)

---

## 🔗 Referensi

- [Recovery options in Windows (Microsoft Support)](https://support.microsoft.com/en-us/windows/recovery-options-in-windows-31ce2444-7de3-818c-d626-e3b5a3024da5)

---

**Tags**: #windows #windows11 #downgrade #rollback #troubleshooting
**Level**: 🟡 Intermediate

**Terakhir diupdate**: 2025-12-09
