# 🤝 Contributing Guide

Terima kasih mau kontribusi ke Tech Tips! 🎉

## 📝 Cara Kontribusi

### 1. Fork & Clone

```bash
# Fork repository ini di GitHub
# Lalu clone ke local:
git clone https://github.com/YOUR_USERNAME/tech-tips.git
cd tech-tips
```

### 2. Buat File Baru

Pilih kategori yang sesuai dan buat file `.md` baru:

```text
tech-tips/
├── windows/
├── linux/
├── networking/
├── software/
└── life-hacks/
```

### 3. Ikuti Template

Copy dari `TEMPLATE.md` dan isi dengan konten kamu:

```bash
cp TEMPLATE.md networking/nama-tips-kamu.md
```

### 4. Format Konten

Pastikan mengikuti format:

```markdown
# [Judul yang Jelas dan Deskriptif]

## 🔍 Masalah
Deskripsi masalah

## ✅ Solusi
Langkah-langkah penyelesaian

## 💡 Penjelasan
Kenapa solusi ini work (opsional)

## 🔗 Referensi
Link ke sumber (opsional)
```

### 5. Update Index

Tambahkan link ke file kamu di `INDEX.md` kategori yang sesuai:

```markdown
### Kategori
- [Judul Tips Kamu](./nama-file.md)
```

### 6. Commit & Push

```bash
git add .
git commit -m "feat: add [nama tips]"
git push origin main
```

### 7. Create Pull Request

Buat PR di GitHub dengan deskripsi singkat tentang tips yang kamu tambahkan.

---

## ✅ Checklist Sebelum Submit

- [ ] File ada di kategori yang tepat
- [ ] Mengikuti format template
- [ ] Judul jelas dan deskriptif
- [ ] Langkah-langkah mudah diikuti
- [ ] Sudah ditest dan work
- [ ] Link ditambahkan di INDEX.md
- [ ] Tidak ada typo

---

## 📋 Guidelines

### Do's ✅

- Tulis dengan bahasa yang simple dan mudah dipahami
- Berikan contoh konkret dan screenshot kalau perlu
- Sertakan command/code yang bisa langsung dicopy
- Tambahkan referensi ke sumber resmi
- Tentukan **Level** kesulitan:
  - 🟢 **Easy**: Tinggal klik-klik, aman, gak pake mikir keras
  - 🟡 **Intermediate**: Butuh otak-atik dikit (CMD, Check IP, Config ringan)
  - 🔴 **Advanced**: Resiko tinggi, buat yang ngerti aja (Registry, Hardware)
- Update tanggal di akhir file

### Don'ts ❌

- Jangan pakai bahasa yang terlalu teknis
- Jangan assume pembaca sudah expert
- Jangan lupa test solusi sebelum submit
- Jangan copy-paste tanpa credit sumber

---

## 🎯 Topik yang Dibutuhkan

Lagi butuh kontribusi untuk:

- [ ] Windows troubleshooting umum
- [ ] Linux command line basics
- [ ] Networking untuk pemula

- [ ] Productivity hacks

---

## 💬 Butuh Bantuan?

Kalau ada pertanyaan atau bingung, feel free untuk:

1. Open issue di GitHub
2. Hubungi maintainer
3. Diskusi di PR comments

---

**Happy Contributing!** 🚀
