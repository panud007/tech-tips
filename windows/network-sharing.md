# Mengatasi Network Sharing Error (Access Denied / Tidak Bisa Connect)

## 🔍 Masalah

Mau akses folder sharing teman kantor (`\\IP-Address` atau `\\Nama-PC`), tapi muncul error:

- "Windows cannot access \\..."
- "You do not have permission to access..."
- Minta username password terus padahal sudah benar.

---

## ✅ Solusi

Cek 3 settingan keramat ini di PC **TUJUAN** (PC yang punya folder) dan PC **KAMU**.

### 1. Advanced Sharing Settings (Wajib)

1. Control Panel > Network and Sharing Center > **Change advanced sharing settings**.
2. Di profil **Private** dan **Guest/Public**:
   - ✅ Turn on network discovery
   - ✅ Turn on file and printer sharing
3. Di profil **All Networks** (Paling bawah):
   - ✅ **Turn off password protected sharing** (Kalau mau sharing tanpa password/login).

### 2. SMB 1.0 Support (Untuk Printer/Windows Jadul)

Kalau connect ke PC Windows 7 atau Printer sharing lama, fitur ini sering mati di Windows 10/11.

1. Start > Ketik "Turn Windows features on or off".
2. Cari **SMB 1.0/CIFS File Sharing Support**.
3. Centang **SMB 1.0/CIFS Client**.
4. OK > Restart Laptop.

### 3. Folder Permission

Pastikan foldernya sudah di-share dengan benar di PC Tujuan:

1. Klik kanan folder > Properties > **Sharing**.
2. Klik **Share...**
3. Pilih "Everyone" -> Add.
4. Set Permission Level: **Read/Write**.
5. Klik **Share**.

---

## 💡 Tips Pro: Map Network Drive

Biar gak capek ketik IP terus, jadikan drive permanen (Drive Z: dll).

1. Buka File Explorer > Klik kanan **This PC** > **Map network drive**.
2. Pilih Drive letter (misal Z:).
3. Folder: `\\192.168.1.50\DataKantor` (Sesuaikan IP & Nama Folder).
4. Centang "Reconnect at sign-in".
5. Finish.

---

## 🎥 Video Tutorial

- [Cara Sharing Folder LAN Windows 10/11 - Gampang Banget](https://www.youtube.com/results?search_query=cara+sharing+folder+lan+windows+10)

---

**Tags**: #windows #network #sharing #smb #lan
**Level**: 🟡 Intermediate

**Terakhir diupdate**: 2025-12-09
