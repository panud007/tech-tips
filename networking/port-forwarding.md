# Port Forwarding Setup (Akses PC dari Luar Rumah)

## 🔍 Masalah

Punya server CCTV, Minecraft Server, atau Web Server di rumah, tapi gak bisa diakses teman dari luar (beda jaringan).

---

## ✅ Konsep Dasar

Router itu kayak satpam. Secara default, dia blokir semua tamu dari luar. **Port Forwarding** itu kayak ngasih memo ke satpam:
*"Pak Satpam, kalau ada tamu ngetok di Pintu 80 (HTTP), tolong anterin langsung ke Kamar Nomor 192.168.1.10 ya."*

---

## ⚙️ Cara Setup Umum

1. **Static IP**: Pastikan PC/Server kamu IP-nya tetap (Static), misal `192.168.1.100`.
2. Login ke **Admin Router**.
3. Cari menu **Forwarding**, **Virtual Server**, atau **Port Forwarding**.
4. Klik **Add New**.
5. Isi data:
   - **Service Port**: Port berapa yang mau dibuka (misal `25565` buat Minecraft).
   - **IP Address**: IP PC kamu (`192.168.1.100`).
   - **Protocol**: TCP/UDP (Pilih ALL kalau bingung).
   - **Status**: Enabled.
6. Save.

---

## 🚫 Perhatian Keamanan

Membuka port = membuka celah keamanan. Hacker bisa masuk kalau server kamu gak dipupuk password kuat. **Jangan buka port RDP (3389) ke publik** sembarangan kalau gak mau kena ransomware!

---

**Tags**: #networking #portforwarding #server #router #advanced
**Level**: 🔴 Advanced
