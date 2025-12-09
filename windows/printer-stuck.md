# Mengatasi Printer Macet / Tidak Mau Print (Stuck in Queue)

## 🔍 Masalah

Printer statusnya "Ready", tapi pas di-print diam saja. Atau ada dokumen nyangkut di "Print Queue" (antrian) yang tidak bisa di-cancel atau di-delete.

Masalah ini biasanya disebabkan oleh service **Print Spooler** yang error atau hang.

---

## ✅ Solusi

Solusi paling ampuh adalah **Restart Print Spooler** dan hapus file antrian sementaranya.

### Cara Cepat (Pakai CMD)

1. Buka **Command Prompt (CMD)** sebagai **Administrator**.
2. Ketik perintah berikut satu per satu (tekan Enter setiap baris):

```cmd
net stop spooler
del /Q /F /S "%systemroot%\System32\Spool\Printers\*.*"
net start spooler
```

1. Coba print ulang. Beres!

### Cara Manual (Lewat Services.msc)

1. Tekan `Win + R`, ketik `services.msc`, Enter.
2. Cari service bernama **Print Spooler**.
3. Klik kanan > **Stop**.
4. Biarkan window Services terbuka, sekarang tekan `Win + R` lagi.
5. Paste path ini: `C:\Windows\System32\spool\PRINTERS` -> Enter.
6. Hapus **SEMUA file** di dalam folder tersebut.
7. Kembali ke window Services, klik kanan **Print Spooler** > **Start**.

---

## 💡 Penjelasan

- **Print Spooler** adalah "tukang pos" di Windows yang mengatur antrian dokumen ke printer.
- Folder `PRINTERS` adalah "kotak surat"-nya. Kalau ada file corrupt di situ, tukang posnya macet.
- Dengan cara di atas, kita paksa berhenti tukang posnya, buang surat yang bikin macet, lalu suruh dia kerja lagi.

---

## 🎥 Video Tutorial

- [Cara Mengatasi Printer Pending / Error Printing - Tutorials](https://www.youtube.com/results?search_query=cara+mengatasi+printer+pending+error+printing)

---

**Tags**: #windows #printer #printing #spooler #cmd
**Level**: 🟢 Easy

**Terakhir diupdate**: 2025-12-09
