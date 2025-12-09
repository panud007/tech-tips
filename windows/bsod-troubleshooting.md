# Blue Screen of Death (BSOD) Troubleshooting

## 🔍 Masalah

Layar tiba-tiba biru dengan emotikon sedih :( dan PC restart sendiri.
Ada kode error seperti:

- `CRITICAL_PROCESS_DIED`
- `MEMORY_MANAGEMENT`
- `IRQL_NOT_LESS_OR_EQUAL`

---

## ✅ Solusi

Jangan panik! BSOD adalah cara Windows melindungi diri biar hardware gak rusak.

### 1. Cek Kode Error (Penting!)

Foto layar pas BSOD atau ingat kodenya. Kode itu kuncinya.

- **Scan QR Code** di layar biru pake HP, biasanya langsung diarahkan ke solusi spesifik Microsoft.

### 2. Update Driver

Penyebab paling umum (70%) adalah driver bentrok.

- Update **VGA Driver** (Nvidia/AMD/Intel).
- Cek **Device Manager**, kalau ada tanda seru kuning (!), klik kanan > Update driver.

### 3. Cek RAM (Memory Diagnostic)

Kalau errornya `MEMORY_MANAGEMENT`:

1. Tekan `Win + R`, ketik `mdsched.exe`.
2. Pilih **Restart now and check for problems**.
3. PC bakal restart dan scan RAM. Kalau ada error, berarti RAM kotor/rusak (coba cabut-pasang/bersihkan kuningan RAM pakai penghapus).

### 4. Repair System Files (SFC & DISM)

Kalau ada file Windows yang corrupt.
Buka CMD (Admin), jalankan:

```cmd
sfc /scannow
```

Tunggu sampai 100%. Kalau masih error, jalankan:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

---

## 💡 Penjelasan

BSOD terjadi karena kernel Windows bingung harus ngapain (biasanya karena ditipu sama driver yang ngasih instruksi salah, atau hardware yang ngasih data corrupt).

---

## 🎥 Video Tutorial

- [Cara Mengatasi Blue Screen Windows 10/11 - Seputar TI](https://www.youtube.com/results?search_query=cara+mengatasi+blue+screen+windows+10)

---

**Tags**: #windows #bsod #bluescreen #crash #error
**Level**: 🔴 Advanced

**Terakhir diupdate**: 2025-12-09
