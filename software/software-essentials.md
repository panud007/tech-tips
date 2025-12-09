# Software Fixes: Browser & Office Troubleshooting

## 🔍 Masalah

Aplikasi sehari-hari yang sering bikin emosi:

1. **Chrome/Browser**: Lemot, makan RAM 90%, atau banyak iklan aneh.
2. **Microsoft Office**: Excel not responding, Word corrupt, atau lupa save.

---

## 🌐 Browser Troubleshooting (Chrome/Edge)

### 1. Browser Lemot & Boros RAM

Browser modern memang rakus RAM, tapi bisa dijinakkan.

- **Update Browser**: Cek `Help > About Google Chrome`. Update fix memory leak.
- **Matikan "Hardware Acceleration"**:
  - Settings > System > Turn off "Use graphics acceleration when available".
  - Ini sering bikin browser nge-freeze di PC spek kentang.
- **Pakai Extension "OneTab"**:
  - Menghemat 95% memori dengan mengubah semua tab jadi satu list.

### 2. Bersihkan Cache & Cookies (Solusi Website Error)

Kalau ada web yang tampilannya berantakan atau gagal login:

1. Tekan `Ctrl + Shift + Delete`.
2. Pilih Time range: **All time**.
3. Centang **Cached images and files** dan **Cookies**.
4. Clear data.

---

## 📄 Office Troubleshooting (Word/Excel)

### 1. Excel/Word "Not Responding"

Biasanya karena Add-ins yang konflik.

1. Buka aplikasi dalam **Safe Mode**:
   - Tahan tombol `CTRL` di keyboard, lalu klik icon Excel/Word.
   - Klik "Yes" saat ditanya Safe Mode.
2. Kalau lancar di Safe Mode, berarti Add-ins masalahnya.
   - File > Options > Add-ins > Go > Uncheck semua.

### 2. Dokumen Lupa Save / Corrupt

Cari file backup otomatis Office:

1. Buka Word/Excel kosong.
2. File > Open > **Recover Unsaved Workbooks/Documents** (tombol di paling bawah).
3. Atau cek folder:
   `C:\Users\%username%\AppData\Local\Microsoft\Office\UnsavedFiles`

---

## 💡 Penjelasan

- **Hardware Acceleration**: Memaksa GPU kerja buat render web. Kalau driver VGA kurang oke, malah bikin berat/crash.
- **Safe Mode**: Mode "polos" tanpa plugin/extension. Cara terbaik buat diagnosa masalah software.

---

**Tags**: #software #chrome #office #excel #word #troubleshooting
**Level**: 🟢 Easy

**Terakhir diupdate**: 2025-12-09
