---
layout: default
---

# RPS sebagai Deliverable Final

**RPS bukan sekadar input — ia juga output yang harus dipoles.**

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## RPS sebagai Suplemen Buku

RPS final yang sinkron dengan buku Anda harus:
- ✅ Nomor bab di RPS = nomor bab di buku
- ✅ Istilah di RPS = istilah di buku (konsisten)
- ✅ Referensi di RPS = ada di daftar pustaka buku
- ✅ Asesmen di RPS = latihan soal di buku

Ini adalah value tambah yang membedakan buku Anda dari buku ajar generik.

</div>
<div>

## Menghasilkan RPS Final dengan AI

```text
Konteks: [rps-konteks.md]
Buku sudah selesai dengan struktur bab: [lampiran]

Tugas: Perbarui RPS agar sinkron 100%
dengan buku. Pastikan:
1. Materi tiap pertemuan = sub-bab di buku
2. Referensi RPS = daftar pustaka buku
3. Asesmen mengacu soal latihan di buku

Output: Tabel RPS lengkap format markdown,
siap dimasukkan ke template prodi.
```

</div>
</div>

<!--
RPS yang sinkron dengan buku adalah nilai jual utama: dosen menggunakan buku sendiri sebagai pegangan, dan mahasiswa tahu persis halaman mana yang relevan untuk setiap pertemuan.
Ini juga memperkuat argumen bahwa buku ini "layak ISBN" karena digunakan secara luas, bukan hanya untuk satu kelas.
-->

---
layout: default
---

# Slide Kuliah dari Buku

**Satu buku → ratusan slide yang konsisten secara otomatis.**

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div>

## Prinsip Slide yang Baik
- Satu ide utama per slide
- Maks. 5 poin per slide
- Visual > teks panjang
- Speaker notes = narasi lengkap

## Workflow
1. Pilih sub-bab dari buku
2. Kirim ke AI dengan instruksi slide
3. AI hasilkan markdown slide
4. Anda validasi & beri speaker notes

</div>
<div>

<div class="border rounded-lg p-3 bg-blue-50 text-sm">

**💬 Contoh Prompt:**
```text
Ubah Sub-bab [x.y] berikut menjadi
slide presentasi:

[tempel konten sub-bab]

Ketentuan:
- Format: markdown Slidev/Marp
- Satu ide per slide
- Maks 5 bullet per slide
- Sertakan speaker notes
  singkat dalam bahasa Indonesia
- Output: blok kode ```md siap tempel
```

</div>

</div>
</div>

<div class="mt-2 border-l-4 border-yellow-400 pl-4 text-sm">
  <strong>💡 Contoh berlabel:</strong> Beberapa AI agentik (khususnya yang berbasis CLI dengan akses file) dapat membaca seluruh folder buku Anda dan menghasilkan semua slide sekaligus dalam format <strong>Slidev atau Marp</strong> — termasuk deploy otomatis ke GitHub Pages. Fitur ini tidak tersedia di semua tool.
</div>

<!--
Labeled example: AI CLI dengan akses file + kemampuan generate Slidev/Marp markdown adalah fitur unik yang sangat menghemat waktu.
Versi manual (copy-paste per sub-bab) bisa dilakukan di tool manapun.
-->

---
layout: default
---

# Pitfalls Slide Kuliah

<div class="grid grid-cols-3 gap-4 mt-4">

<div class="border rounded-lg p-4 border-red-300">
<h3 class="font-bold text-red-700">1. 📄 Wall of Text</h3>
<p class="text-sm mt-2">AI cenderung memindahkan paragraf dari buku ke slide tanpa menyederhanakan.</p>
<p class="text-sm mt-2"><strong>Solusi:</strong> Tambahkan instruksi: "Maks 5 poin. Setiap poin maks 10 kata."</p>
</div>

<div class="border rounded-lg p-4 border-orange-300">
<h3 class="font-bold text-orange-700">2. 📊 Tanpa Narasi</h3>
<p class="text-sm mt-2">Slide tanpa speaker notes = kertas contekan, bukan alat presentasi.</p>
<p class="text-sm mt-2"><strong>Solusi:</strong> Selalu minta speaker notes. Atau tulis narasi Anda sendiri berdasarkan bab.</p>
</div>

<div class="border rounded-lg p-4 border-yellow-300">
<h3 class="font-bold text-yellow-700">3. 🔗 Tidak Ada Alur Cerita</h3>
<p class="text-sm mt-2">Kumpulan fakta ≠ presentasi. Slide butuh arc: pembuka → isi → penutup.</p>
<p class="text-sm mt-2"><strong>Solusi:</strong> Tambahkan slide "Hook" di awal dan "Ringkasan" di akhir setiap bab.</p>
</div>

</div>

<div class="mt-3 border rounded-lg p-3 bg-green-50 text-sm">
  <strong>💡 Tips:</strong> Gunakan rumus <em>"Hook → Isi → Takeaway"</em> untuk setiap sesi kuliah. Minta AI mengikuti struktur ini saat menghasilkan slide.
</div>

<!--
Slide yang baik adalah presentasi, bukan buku yang dicetak kecil.
Tekankan: tugas AI adalah membuat draft slide yang efisien — tugas dosen adalah memastikan alur narasi tetap ada.
-->

---
layout: default
---

# Skill & Kapabilitas yang Mempercepat Buku Teknis

*Kapabilitas ini bersifat agnostik — berlaku di AI tool manapun.*

<div class="grid grid-cols-3 gap-3 mt-4 text-sm">

<div class="border rounded-lg p-3">
<h3 class="font-bold">🗂️ Outline & Struktur</h3>
<p class="mt-2">Generate peta bab dari RPS, usulkan urutan sub-bab, identifikasi gap konten sebelum mulai menulis.</p>
</div>

<div class="border rounded-lg p-3">
<h3 class="font-bold">📝 Konsistensi Glosarium</h3>
<p class="mt-2">Cek istilah lintas bab, standardisasi terminologi, bandingkan dengan glosarium proyek.</p>
</div>

<div class="border rounded-lg p-3">
<h3 class="font-bold">🔖 Penanda Sitasi</h3>
<p class="mt-2">Tandai <code>[SITASI?]</code> & <code>[VERIFIKASI]</code> otomatis di setiap klaim faktual — cegah referensi palsu.</p>
</div>

<div class="border rounded-lg p-3">
<h3 class="font-bold">🔄 Konversi Format</h3>
<p class="mt-2">Markdown → DOCX → PDF → Slide (Slidev/Marp). Satu naskah, banyak output format.</p>
</div>

<div class="border rounded-lg p-3">
<h3 class="font-bold">📊 Tabel & Diagram</h3>
<p class="mt-2">Generate tabel perbandingan, diagram alur ASCII/Mermaid, dan ilustrasi konsep langsung dari teks bab.</p>
</div>

<div class="border rounded-lg p-3">
<h3 class="font-bold">✅ Cek Keterbacaan</h3>
<p class="mt-2">Evaluasi tingkat kesulitan teks, konsistensi gaya penulisan, dan kejelasan kalimat per sub-bab.</p>
</div>

</div>

<!--
Ini adalah "menu kapabilitas" yang bisa dipilih audiens sesuai kebutuhan mereka.
Tekankan: semua ini bisa dilakukan dengan instruksi prompt biasa — tapi tool yang punya Skills bisa menjalankannya satu klik.
-->

---
layout: default
---

# Contoh Skill Konkret: Claude Code & opencode

<div class="mt-3 border-l-4 border-yellow-400 pl-3 text-sm mb-4">
  <strong>💡 Contoh berlabel</strong> — tool-spesifik. Kapabilitas dasarnya (slide sebelumnya) berlaku di AI manapun.
</div>

<div class="grid grid-cols-2 gap-6 text-sm">
<div>

## 🔧 Custom Skills / Slash Commands

Buat perintah reusable untuk workflow buku Anda:

| Skill | Fungsi |
|---|---|
| `/outline-bab` | Generate outline dari RPS + glosarium |
| `/draft-subbab` | Draft 1 sub-bab dengan penanda SITASI? |
| `/cek-sitasi` | Validasi semua referensi di file aktif |
| `/sync-rps` | Sinkronisasi RPS dengan struktur bab final |
| `/gen-slide` | Konversi sub-bab ke format Slidev |

</div>
<div>

## ⚙️ Fitur Agentic Lanjutan

- **Subagents** — proses beberapa bab secara paralel dalam satu sesi
- **File access** — baca seluruh folder proyek buku sekaligus
- **MCP tools** — sambungkan ke database referensi atau Zotero
- **Persistent memory** — CLAUDE.md / project config dimuat otomatis setiap sesi

**Cara mulai:**
```text
Simpan RPS + glosarium dalam folder proyek.
Jalankan: claude "Buat peta bab dari RPS ini"
```

</div>
</div>

<!--
Skills/slash-commands adalah cara paling efisien untuk menyimpan workflow buku yang sudah terbukti dan menjalankannya ulang tanpa mengetik prompt panjang setiap kali.
Arahkan audiens yang tertarik ke dokumentasi Claude Code / opencode untuk membuat skill pertama mereka.
-->
