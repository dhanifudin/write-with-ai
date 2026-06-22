---
layout: default
---

# Tool Landscape: Pilih Berdasarkan Kapabilitas

*Tabel ini agnostik — menilai kemampuan, bukan merek.*

<div class="mt-4 text-sm">

| Kapabilitas | Perlu untuk Buku? | Tool Berbasis Chat | Tool Berbasis CLI/Agen |
|---|:---:|---|---|
| Long context (100K+ token) | ✅ Penting | Sebagian besar mendukung | Sebagian besar mendukung |
| Upload & baca file (PDF/DOCX) | ✅ Penting | Banyak yang sudah bisa | Bisa via tool calling |
| **Persistent project memory** | ⭐ Sangat membantu | Perlu upload ulang tiap sesi | **Beberapa CLI otomatis** |
| Akses & tulis file lokal | 🔧 Untuk workflow maju | ❌ Umumnya tidak | ✅ Biasanya bisa |
| Generate Slidev/Marp markdown | 🔧 Untuk slide otomatis | Perlu prompt manual | Bisa otomatis via file |
| Web search / research | 🔧 Untuk referensi | Bervariasi | Bervariasi |

</div>

<div class="mt-3 border-l-4 border-yellow-400 pl-3 text-sm">
  <strong>💡 Rekomendasi untuk pemula:</strong> Mulai dengan tool berbasis chat yang familiar. Setelah paham alurnya, pertimbangkan tool CLI agentik untuk proyek yang lebih besar — terutama untuk fitur <em>persistent memory</em>.
</div>

<!--
Jangan rekomendasikan satu tool — berikan framework evaluasi. Audiens memiliki konteks dan anggaran berbeda.
-->

---
layout: default
---

# Key Takeaways: Mulai Hari Ini

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## 5 Hal yang Harus Diingat

1. 🤖 **Agentic AI** ≠ chatbot biasa — ia bisa merencanakan, menggunakan tools, dan iterate
2. 📋 **RPS-First** — RPS Anda adalah blueprint buku yang sudah ada
3. 💬 **RTCE Prompt** — Role, Task, Constraints, Examples
4. ⚠️ **Verifikasi SELALU** — terutama referensi & sitasi
5. 📖 **Judul aman ISBN** — hindari Modul, Diktat, Panduan [Internal]

</div>
<div>

## ✅ Checklist Mulai Besok

- [ ] Buka RPS salah satu mata kuliah Anda
- [ ] Buat file `rps-konteks.md` (konteks proyek)
- [ ] Minta AI membuat peta bab dari RPS
- [ ] Validasi struktur bab bersama kolega
- [ ] Tulis draf Bab 1, Sub-bab 1.1
- [ ] Verifikasi semua `[SITASI?]` yang muncul
- [ ] Cek judul: sudah aman ISBN?

</div>
</div>

<div class="mt-4 text-center text-lg font-semibold">
  🎯 "Bukan soal sempurna — soal <em>mulai</em>."
</div>

<!--
Dorong audiens untuk mengambil satu langkah konkret hari ini. Bahkan hanya membuka RPS dan membuat file konteks adalah kemajuan nyata.
-->

---
layout: center
class: text-center
---

# Disclaimer

<div class="mt-6 p-6 border-2 rounded-xl max-w-lg mx-auto">

## 🤖 Presentasi ini 100% ditulis dengan Agentic AI

Seluruh teks, struktur bab, contoh prompt, dan kode Slidev dalam presentasi ini dihasilkan **end-to-end** oleh Agentic AI.

**Peran manusia (pembicara):**
- Memberikan brief, arah, dan batasan
- Memvalidasi setiap fakta (termasuk aturan ISBN Perpusnas)
- Mengedit dan menyesuaikan konten
- Bertanggung jawab penuh atas seluruh isi

</div>

<div class="mt-6 opacity-70 text-sm">
  Ini bukan gimmick — ini adalah <strong>bukti hidup</strong> dari alur kerja yang baru saja diajarkan.<br>
  <em>Dosen sebagai Director. AI sebagai Drafting Collaborator.</em>
</div>

<!--
Ini adalah slide yang paling diingat audiens. Beri jeda sejenak setelah menampilkan slide ini.
Tanyakan: "Apakah tadi Anda merasakan perbedaan kualitas presentasi ini vs presentasi biasa?"
Lalu: "Itulah yang bisa Anda lakukan untuk buku Anda."
-->

---
layout: cover
class: text-center
---

# Terima Kasih

**Dian Hanifudin Subhi**
Jurusan Teknologi Informasi · Politeknik Negeri Malang

linkedin.com/in/dhanifudin · dhanifudin.com

<div class="mt-6 grid grid-cols-3 gap-4 text-sm max-w-lg mx-auto">
<div class="border rounded p-3">
<div class="font-bold">📖 Sumber ISBN</div>
isbn.perpusnas.go.id
</div>
<div class="border rounded p-3">
<div class="font-bold">🎞️ Deck ini</div>
dhanifudin.github.io/<br>write-with-ai
</div>
<div class="border rounded p-3">
<div class="font-bold">💬 Tanya Jawab</div>
Silakan bertanya!
</div>
</div>

<div class="abs-b m-6 text-xs opacity-50">
  Referensi: Juknis Layanan ISBN Perpusnas RI · isbn.perpusnas.go.id · penerbitdeepublish.com/information/daftar-buku-yang-tidak-dapat-diberikan-isbn
</div>

<!--
Buka sesi tanya jawab. Pertanyaan yang sering muncul:
1. "Tool apa yang Anda gunakan?" → Jawab dengan menunjuk ke capability table
2. "Apakah hasil AI perlu diedit banyak?" → Ya, tapi jauh lebih efisien dari menulis dari nol
3. "Apakah kampus saya mengizinkan?" → Cek kebijakan kampus, tren global mengarah ke penerimaan dengan disclosure
-->

---
layout: default
class: prompt-lib
---

# Lampiran 1 — Prompt Library: RPS & Buku Ajar

*Copy-paste langsung. Ganti bagian [dalam kurung kotak] dengan konten Anda.*

```text
[1] SUSUN RPS]
Kamu editor kurikulum perguruan tinggi Indonesia. Dari CPL: [tempel CPL]
Susun RPS mata kuliah "[Nama MK]" 16 pertemuan: CPMK, sub-CPMK, materi,
metode, bobot. Output: tabel markdown. Tandai [VALIDASI] bagian kritis.

[2] RPS → PETA BAB]
Dari RPS terlampir [tempel RPS], usulkan struktur bab buku ajar yang
memetakan 16 pertemuan ke bab/sub-bab logis. Beri outline + alasan urutan.
Jangan tulis konten dulu.

[3] OUTLINE BAB]
Kembangkan outline detail Bab [n]: "[Judul Bab]".
Untuk setiap sub-bab: judul, 2-3 poin utama, estimasi halaman.

[4] DRAFT SUB-BAB]
Kamu penulis buku ajar akademik Indonesia. Konteks: [rps-konteks.md]
Tulis draf Sub-bab [x.y]: "[Judul]". Gaya: akademik tapi mudah dipahami
mahasiswa S1. Sertakan contoh. Tutup dengan ringkasan 3 poin.
Tandai [SITASI?] setiap klaim yang perlu referensi. JANGAN mengarang referensi.

[5] EDIT KONSISTENSI]
Tinjau bab ini [tempel teks]. Berikan: (1) bagian kurang jelas,
(2) klaim tanpa referensi, (3) saran perbaikan spesifik.
Bandingkan juga istilah dengan glosarium: [tempel glosarium].
```

<!--
Slide ini adalah hadiah terbesar untuk audiens — prompt siap pakai yang bisa langsung dicoba.
Sarankan mereka screenshot atau download slide PDF.
-->

---
layout: default
class: prompt-lib
---

# Lampiran 2 — Prompt Library: ISBN, Editing & Slide

```text
[6] JUDUL AMAN ISBN]
Usulkan 5 judul buku layak ISBN untuk topik: [deskripsi topik mata kuliah].
Hindari: 'Modul', 'Diktat', 'Panduan Praktikum', 'untuk Mahasiswa [Prodi]'.
Judul harus terkesan buku umum yang bisa dibeli siapa saja.

[7] KATA PENGANTAR]
Tulis Kata Pengantar buku ajar ini. Fokus pada: (1) apa isi buku,
(2) untuk siapa, (3) struktur bab, (4) cara terbaik menggunakannya.
Maks 400 kata. JANGAN isi dengan ucapan terima kasih.

[8] SLIDE KULIAH]
Ubah Sub-bab [x.y] berikut menjadi slide presentasi: [tempel konten]
Format: markdown Slidev (atau Marp).
Ketentuan: satu ide per slide, maks 5 bullet/slide, maks 10 kata/bullet.
Sertakan speaker notes singkat. Output: blok kode ```md siap tempel.

[9] SINKRONISASI RPS FINAL]
Konteks: [rps-konteks.md]. Buku selesai dengan struktur bab: [lampiran].
Perbarui RPS agar sinkron 100% dengan buku: materi tiap pertemuan = sub-bab,
referensi RPS = daftar pustaka buku. Output: tabel RPS format markdown.

[10] VERIFIKASI REFERENSI]
Dari daftar referensi berikut: [tempel daftar]
Identifikasi referensi yang perlu diverifikasi manual (mungkin tidak valid).
Beri skor keyakinan 1-5 untuk setiap referensi. Jangan menambah referensi baru.
```

<div class="mt-3 text-xs opacity-60">
  📌 Ingat: Semua prompt ini bersifat agnostik — berlaku untuk AI tool apapun yang mendukung teks panjang.
</div>

<!--
Tutup dengan mendorong audiens untuk langsung mencoba Prompt #1 atau #2 setelah sesi ini.
"Tidak perlu sempurna — coba, lihat hasilnya, perbaiki."
-->
