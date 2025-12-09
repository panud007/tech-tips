# WiFi Connected tapi No Internet

## 🔍 Masalah

WiFi sudah connect dan sinyal penuh, tapi tidak bisa browsing atau akses internet. Icon WiFi menunjukkan "Connected, No Internet" atau ada tanda seru kuning.

Gejala:

- WiFi connected tapi browser tidak bisa buka website
- Aplikasi tidak bisa akses internet
- Icon WiFi ada tanda seru/warning
- Device lain di WiFi yang sama bisa internet

---

## ✅ Solusi

### Langkah 1: Restart Router & Device

Cara paling simple dan sering berhasil:

1. **Restart Router**:
   - Cabut kabel power router
   - Tunggu 30 detik
   - Colok kembali
   - Tunggu sampai semua lampu menyala normal

2. **Restart Device**:
   - Restart laptop/HP kamu
   - Reconnect ke WiFi

### Langkah 2: Flush DNS & Reset Network

Kalau restart tidak work, coba reset network settings:

**Windows:**

```powershell
# Buka Command Prompt as Administrator, lalu jalankan:
ipconfig /flushdns
ipconfig /release
ipconfig /renew
netsh winsock reset
netsh int ip reset
```

Setelah itu restart komputer.

**Android:**

1. Settings → Network & Internet → WiFi
2. Tap WiFi yang connected
3. Tap "Forget"
4. Connect ulang dengan password

**iOS:**

1. Settings → General → Transfer or Reset iPhone
2. Reset → Reset Network Settings
3. Connect ulang ke WiFi

### Langkah 3: Ganti DNS

Kadang DNS dari ISP bermasalah. Ganti ke DNS Google atau Cloudflare:

**Windows:**

1. Control Panel → Network and Sharing Center
2. Click WiFi connection → Properties
3. Double-click "Internet Protocol Version 4 (TCP/IPv4)"
4. Pilih "Use the following DNS server addresses"
5. Isi:
   - **Preferred DNS**: `8.8.8.8` (Google) atau `1.1.1.1` (Cloudflare)
   - **Alternate DNS**: `8.8.4.4` (Google) atau `1.0.0.1` (Cloudflare)
6. OK → Close

**Android/iOS:**

1. Settings → WiFi
2. Tap WiFi yang connected
3. Scroll ke DNS settings
4. Ganti manual ke `8.8.8.8` atau `1.1.1.1`

### Langkah 4: Cek APIPA & Set IP Manual

Kalau device kamu menunjukkan status "Connected" tapi IP address-nya berawalan **`169.254.x.x`**, itu tandanya kamu terkena **APIPA** (Automatic Private IP Addressing).

**Apa itu APIPA?**
Ini adalah IP "darurat" yang diberikan sistem operasi (Windows/Android/iOS) saat **gagal mendapatkan IP dari Router/DHCP Server**.

**Penyebab:**

1. DHCP Pool di router penuh (terlalu banyak user)
2. Router hang/error tidak bisa bagi IP
3. Jarak terlalu jauh, request DHCP timeout

**Solusinya:** Set IP secara **Manual (Static)** agar tidak perlu antri DHCP.

**Windows:**

1. Buka Command Prompt, ketik `ipconfig`.
2. Cek apakah IP kamu `169.254.x.x`? Jika ya, lanjut langkah di bawah.
3. Control Panel → Network and Sharing Center
4. Click WiFi connection → Properties
5. Double-click "Internet Protocol Version 4 (TCP/IPv4)"
6. Pilih "Use the following IP address"
7. Isi dengan IP yang tidak bentrok:
   - **IP Address**: `192.168.1.100` (atau sesuai range router kamu)
   - **Subnet Mask**: `255.255.255.0`
   - **Default Gateway**: `192.168.1.1` (IP router kamu)
   - **Preferred DNS**: `8.8.8.8`
   - **Alternate DNS**: `8.8.4.4`
8. OK → Close

**Cara Cek IP Range Router:**

```powershell
# Buka Command Prompt, jalankan:
ipconfig

# Lihat di bagian "Default Gateway" - itu IP router kamu
# Contoh: 192.168.1.1 atau 192.168.0.1
```

**Tips Pilih IP Manual:**

- Kalau gateway `192.168.1.1` → Pakai IP `192.168.1.100` - `192.168.1.254`
- Kalau gateway `192.168.0.1` → Pakai IP `192.168.0.100` - `192.168.0.254`
- Hindari IP `192.168.x.1` - `192.168.x.50` (biasanya sudah dipakai device lain)

**Android:**

1. Settings → WiFi
2. Tap WiFi yang connected → Advanced
3. IP Settings → **Static**
4. Isi IP Address, Gateway, DNS seperti di atas
5. Save

**iOS:**

1. Settings → WiFi
2. Tap (i) di samping WiFi yang connected
3. Configure IP → **Manual**
4. Isi IP Address, Subnet Mask, Router (Gateway)
5. Scroll ke DNS → Isi `8.8.8.8`

---

## 💡 Penjelasan

Masalah "Connected, No Internet" biasanya terjadi karena:

1. **DNS Issue**: Device tidak bisa resolve domain name ke IP address
2. **IP Conflict**: Ada device lain pakai IP yang sama
3. **Router Cache**: Router punya cached data yang corrupt
4. **ISP Problem**: Masalah dari provider internet

Dengan flush DNS dan reset network, kita clear semua cached data dan force device untuk request IP & DNS baru dari router.

---

## ⚠️ Catatan Penting

- Kalau **semua device** tidak bisa internet, masalahnya di router/ISP, bukan di device kamu
- Kalau **hanya device kamu** yang bermasalah, ikuti langkah di atas
- Kalau sudah coba semua tapi masih tidak work, hubungi ISP kamu

---

## 🔗 Referensi

- [Microsoft Network Troubleshooting](https://support.microsoft.com/en-us/windows/fix-wi-fi-connection-issues-in-windows-9424a1f7-6a3b-65a6-4d78-7f07eee84d2c)
- [Google Public DNS](https://developers.google.com/speed/public-dns)
- [Cloudflare DNS](https://1.1.1.1/)

---

**Tags**: #windows #networking #wifi #dns #troubleshooting
**Level**: 🟡 Intermediate

**Terakhir diupdate**: 2025-12-09
