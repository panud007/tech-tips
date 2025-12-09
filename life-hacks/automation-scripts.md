# Automation dengan Simple Scripts (.bat)

## 🔍 Masalah

Tiap pagi harus buka 5 aplikasi kerja (Chrome, Slack, Spotify, Outlook, Excel) satu-satu. Ribet dan buang waktu.

---

## ✅ Solusi: Batch File (.bat)

Kamu bisa bikin satu file kecil yang kalau diklik 2x, langsung ngerjain tugas rutin itu.

### Cara Buat "Morning Routine" Script

1. Buka **Notepad**.
2. Copy code ini:

```batch
@echo off
echo Selamat Pagi! Sedang membuka aplikasi kerja...

:: Buka Chrome Website Kantor
start chrome "https://mail.google.com" "https://trello.com"

:: Buka Aplikasi (Sesuaikan path aplikasinya)
start "" "C:\Users\Username\AppData\Local\Slack\slack.exe"
start "" "C:\Program Files\Microsoft Office\root\Office16\OUTLOOK.EXE"

:: Buka Folder Project
start explorer "D:\Data Kantor\Project 2024"

echo Selesai! Semangat kerjanya!
pause
```

3. **File > Save As**.
4. Ubah "Save as type" jadi **All Files (*.*)**.
5. Kasih nama `MulaiKerja.bat`.
6. Taruh di Desktop. Klik 2x tiap pagi. 😎

---

## 💡 Ide Lain

- Script buat **Auto Shutdown** ( `shutdown -s -t 3600` untuk matiin 1 jam lagi).
- Script buat **Backup Data** (Copy folder A ke Flashdisk).

---

**Tags**: #lifehacks #automation #coding #script #windows
**Level**: 🟡 Intermediate
