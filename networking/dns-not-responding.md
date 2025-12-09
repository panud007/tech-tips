# DNS Server Not Responding / No Internet

## 🔍 Masalah

WiFi connect, tapi browsing gagal.

- Chrome error: `DNS_PROBE_FINISHED_NXDOMAIN`
- Troubleshooter bilang: "DNS Server is not responding".

---

## ✅ Solusi

### 1. Flush DNS (Bersihkan Cache)

1. Buka CMD (Admin).
2. Ketik: `ipconfig /flushdns` -> Enter.
3. Ketik: `ipconfig /release` -> Enter (Internet putus).
4. Ketik: `ipconfig /renew` -> Enter (Internet nyambung lagi).

### 2. Reset Winsock (Reset Jaringan Total)

Kalau flush gak mempan, reset katalog jaringan di Windows.

1. Di CMD (Admin), ketik:
   `netsh winsock reset`
2. **WAJIB RESTART LAPTOP**.

---

## 💡 Penjelasan

DNS (Domain Name System) itu buku telepon internet. Kalau DNS error, komputer gak tau `google.com` itu alamat IP-nya berapa. Flush DNS = buang buku telepon lama dan minta yang baru.

---

**Tags**: #networking #dns #error #internet #cmd
**Level**: 🟡 Intermediate
