# Dari RPS ke Buku ber-ISBN dengan AI Agentik

> **🤖 Presentasi ini 100% ditulis dengan Agentic AI.**
> Seluruh teks, struktur, contoh prompt, dan kode Slidev dihasilkan end-to-end oleh Agentic AI.
> Pembicara bertindak sebagai director/editor — memvalidasi, mengarahkan, dan bertanggung jawab penuh atas isi.

Presentasi Slidev untuk dosen yang ingin menerbitkan buku ajar ber-ISBN menggunakan Agentic AI, dengan RPS (Rencana Pembelajaran Semester) sebagai sumber kebenaran (*single source of truth*).

**Target audiens:** Dosen, level pemula  
**Durasi:** ~45–60 menit  
**Bahasa:** Bilingual (Indonesia + English technical terms)

---

## 🚀 Menjalankan Secara Lokal

```bash
# 1. Install dependencies
npm install

# 2. Jalankan dev server (buka otomatis di browser)
npm run dev
# → Buka http://localhost:3030
```

## 📦 Build untuk GitHub Pages

```bash
# Build dengan base path sesuai nama repo
npm run build -- --base /write-with-ai/

# Hasil ada di folder dist/
```

## 📄 Export ke PDF

```bash
npm run export
# Menghasilkan file PDF di folder saat ini
```

---

## 🌐 Deploy ke GitHub Pages

### Otomatis via GitHub Actions

Workflow sudah dikonfigurasi di `.github/workflows/deploy.yml`.

**Langkah satu kali:**
1. Push repo ke GitHub
2. Buka **Settings → Pages → Source: GitHub Actions**
3. Setiap push ke branch `main` akan otomatis build & deploy

**URL setelah deploy:** `https://<username>.github.io/write-with-ai/`

> **Catatan:** Jika menggunakan custom domain atau repo `<username>.github.io`, ganti `--base /write-with-ai/` menjadi `--base /` di `deploy.yml`.

---

## 📁 Struktur File

```
write-with-ai/
├── slides.md              # Entry point — global config + src includes
├── pages/
│   ├── 00-cover.md        # Intro (slides 1-3)
│   ├── 01-fondasi.md      # Fondasi: Apa itu Agentic AI?
│   ├── 02-rps-first.md    # RPS-First Approach
│   ├── 03-alur.md         # Alur Menulis Universal
│   ├── 04-prompt.md       # Teknik Prompt & Context
│   ├── 05-buku-ajar.md    # Playbook: Buku Ajar
│   ├── 06-isbn.md         # ISBN: Aturan & Checklist
│   ├── 07-rps-output.md   # RPS Final + Slide Kuliah
│   ├── 08-kualitas.md     # Kualitas, Etika & Praktik
│   └── 09-penutup.md      # Penutup + Prompt Library
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Pages deploy workflow
└── package.json
```

---

## 📚 Referensi ISBN

- [Portal ISBN Perpusnas RI](https://isbn.perpusnas.go.id/)
- [Petunjuk Teknis Layanan ISBN Perpusnas](https://jdih.perpusnas.go.id/file_juknis/Petunjuk_Teknis_Layanan_ISBN.pdf)
- [Daftar buku yang tidak dapat ISBN (Deepublish)](https://penerbitdeepublish.com/information/daftar-buku-yang-tidak-dapat-diberikan-isbn/)

> ⚠️ Kebijakan ISBN dapat berubah. Selalu verifikasi ke portal resmi Perpusnas sebelum mengajukan.
