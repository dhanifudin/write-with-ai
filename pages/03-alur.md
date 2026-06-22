---
layout: section
---

# Bagian 3
## Alur Menulis Universal

*Pipeline: RPS → Buku → Terbit*

<!--
Bagian ini membahas alur lengkap dari RPS sampai buku siap terbit. Tekankan bahwa ini bukan proses linear yang kaku — AI membantu di setiap tahap.
-->

---
layout: default
---

# Pipeline: Dari RPS ke Buku Terbit

```
 RPS          Outline       Draft        Edit        Publish
  │             │             │            │            │
  ▼             ▼             ▼            ▼            ▼
Peta Bab ──► Sub-bab ───► Per bab ───► Revisi ───► ISBN + PDF
              & topik       1 per 1     & cek       & Cetak
                           sesi        sitasi
```

<div class="grid grid-cols-5 gap-2 mt-6 text-center text-sm">
<div class="border rounded p-2 bg-green-50">
<strong>RPS</strong><br>
Upload konteks, buat peta bab
</div>
<div class="border rounded p-2 bg-blue-50">
<strong>Outline</strong><br>
Struktur bab & sub-bab
</div>
<div class="border rounded p-2 bg-yellow-50">
<strong>Draft</strong><br>
Tulis satu sub-bab per sesi
</div>
<div class="border rounded p-2 bg-orange-50">
<strong>Edit</strong><br>
Konsistensi, sitasi, nada
</div>
<div class="border rounded p-2 bg-purple-50">
<strong>Publish</strong><br>
ISBN, format, cetak
</div>
</div>

<!--
Pipeline ini adalah panduan kerja nyata. Tekankan: kerjakan satu bab dulu sampai selesai sebelum pindah ke bab berikutnya — jangan loncat-loncat.
Setiap tahap punya prompt yang berbeda, dan akan dibahas satu per satu.
-->

---
layout: default
---

# Outlining Buku dari RPS

**Prinsip:** Validasi struktur sebelum mengisi konten.

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## Yang Dilakukan AI
- Usul struktur bab berdasarkan peta pertemuan
- Tentukan sub-bab per bab
- Perkirakan bobot halaman per bab
- Identifikasi topik yang tumpang tindih

</div>
<div>

## Yang Dilakukan Dosen
- ✅ Validasi urutan logis
- ✅ Sesuaikan dengan standar prodi
- ✅ Tambah/hapus sub-topik
- ✅ Setujui sebelum lanjut ke draft

</div>
</div>

<div class="mt-4 border rounded-lg p-3 bg-blue-50 text-sm">

**💬 Contoh Prompt:**
```text
Dari peta bab terlampir, kembangkan outline detail untuk Bab [n].
Untuk setiap sub-bab, berikan:
- Judul sub-bab
- 2-3 poin utama yang dibahas
- Estimasi panjang (halaman)
Jangan tulis konten dulu — outline saja.
```

</div>

<!--
Tekankan: outlining adalah investasi yang menghemat banyak waktu di tahap drafting.
Bab yang dimulai tanpa outline sering "melantur" dan harus ditulis ulang.
-->

---
layout: default
---

# Drafting Per Bab

**Prinsip:** Satu sub-bab per sesi. Konteks selalu dibawa.

<div class="mt-4 border rounded-lg p-4 bg-blue-50">

**💬 Contoh Prompt — Drafting:**
```text
Kamu adalah penulis buku ajar akademik Indonesia.

Konteks proyek: [tempel rps-konteks.md]

Tugas: Tulis draf Sub-bab [x.y] — "[Judul Sub-bab]"
sesuai outline yang sudah disetujui.

Ketentuan:
- Gaya akademik tapi mudah dipahami mahasiswa S1
- Sertakan minimal 1 contoh konkret
- Tutup dengan ringkasan 3 poin
- Gunakan istilah sesuai glosarium terlampir
- Tandai dengan [SITASI?] setiap klaim yang butuh
  referensi — JANGAN mengarang referensi sendiri

Target panjang: ~800-1000 kata
```

</div>

<!--
Penanda [SITASI?] adalah teknik penting: memaksa AI untuk jujur ketika butuh referensi, alih-alih mengarang.
"Jangan mengarang referensi" harus selalu ada di prompt drafting — ini adalah masalah terbesar AI untuk buku akademik.
-->

---
layout: default
---

# Editing & Konsistensi

**Setelah semua bab selesai draf, lakukan editing pass.**

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## Pass 1 — Per Bab
- Cek logika & kelengkapan
- Verifikasi semua `[SITASI?]` secara manual
- Pastikan contoh relevan & akurat

```text
"Tinjau bab ini dan berikan:
1. Bagian yang kurang jelas
2. Klaim tanpa referensi
3. Saran perbaikan spesifik"
```

</div>
<div>

## Pass 2 — Lintas Bab
- Konsistensi istilah
- Nada & gaya penulisan seragam
- Transisi antar bab

```text
"Bandingkan definisi istilah [X]
di Bab 2 dan Bab 4. Apakah
konsisten? Sarankan perbaikan."
```

</div>
</div>

<!--
Editing dengan AI paling efektif dilakukan dalam dua pass: dulu per bab (konten), lalu lintas bab (konsistensi).
Jangan gabungkan keduanya — fokus yang berbeda membutuhkan prompt yang berbeda.
-->

---
layout: default
---

# Publishing & Sitasi

**Tahap akhir: format, sitasi, dan persiapan ISBN.**

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## Format Export
- 📄 **PDF** — untuk pengajuan ISBN & cetak
- 📝 **DOCX** — untuk editor penerbit
- 🌐 **HTML/ePub** — untuk versi digital

Gunakan template Word/LaTeX dari penerbit Anda sebagai referensi format.

</div>
<div>

## Sitasi & Referensi
- Minta AI dalam format **APA / IEEE / Chicago**
- **SELALU verifikasi** setiap referensi secara manual
- Gunakan Mendeley/Zotero sebagai ground truth

```text
"Konversi daftar referensi ini
ke format APA 7th edition.
Output: daftar siap tempel."
```

</div>
</div>

<div class="mt-4 p-3 border-l-4 border-red-400 text-sm">
  ⚠️ <strong>Peringatan:</strong> AI sering mengarang judul artikel, volume, halaman, atau DOI yang tidak ada. Verifikasi SETIAP referensi di Google Scholar / Scopus sebelum submit ke penerbit.
</div>

<!--
Sitasi palsu (hallucinated references) adalah masalah #1 buku akademik yang ditulis dengan AI.
Tekankan: AI sangat bagus membantu FORMAT sitasi, tapi tidak bisa dipercaya untuk menggenerate referensi baru.
-->
