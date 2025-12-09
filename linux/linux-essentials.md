# Linux Essentials: Permissions, Services & Disk

## 🔍 Masalah Umum

1. **Permission Denied**: Gak bisa edit file atau jalanin script.
2. **Service Error**: Webserver atau database mati/gagal start.
3. **Disk Full**: Server tiba-tiba lemot atau error "No space left on device".

---

## ✅ Solusi 1: Permissions (Hak Akses)

### Fix "Permission Denied"

Gunakan `chmod` untuk ubah mode, dan `chown` untuk ubah pemilik.

```bash
# Berikan akses Read/Write/Execute ke Owner, Read/Execute ke Group/Others
chmod 755 nama_file

# Atau kalau mau full akses (Hati-hati!)
chmod 777 nama_file

# Ubah kepemilikan file ke user 'www-data' (biasanya untuk Web Server)
chown -R www-data:www-data /var/www/html
```

## ✅ Solusi 2: Services Management

### Cek, Start, Stop Service

Pakai `systemctl`. Contoh untuk Nginx/Apache/MySQL:

```bash
# Cek status (Error log biasanya muncul disini)
sudo systemctl status nginx

# Start / Stop / Restart
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
```

### Cek Error Log

Kalau service gagal start, cek log detailnya:

```bash
journalctl -xe
# Atau baca log spesifik
tail -f /var/log/nginx/error.log
```

## ✅ Solusi 3: Disk Space Management

### Cek Kapasitas Disk

```bash
df -h
```

Lihat kolom **Use%**. Kalau ada yang 100%, itu masalahnya.

### Cari File Besar

Cari folder mana yang makan tempat:

```bash
# Scan dari root, cari folder terbesar
du -sh /* | sort -hr
```

### Bersihkan Cache (Ubuntu/Debian)

```bash
sudo apt-get clean
sudo apt-get autoremove
```

---

## 💡 Penjelasan

- **755 vs 777**: 755 aman (public cuma bisa baca/run), 777 bahaya (public bisa edit/hapus).
- **Service**: Program yang jalan di background. Kalau config salah dikit aja, dia bakal refuse to start.
- **Disk Full**: Sering kejadian karena log file yang membengkak (`/var/log`).

---

**Tags**: #linux #permission #chmod #systemctl #disk-space
**Level**: 🟡 Intermediate

**Terakhir diupdate**: 2025-12-09
