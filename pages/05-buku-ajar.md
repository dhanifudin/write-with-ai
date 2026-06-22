---
layout: section
---

# Bagian 5
## Playbook Akademik

*Buku Ajar · ISBN · Slide Kuliah*

<!--
Bagian ini adalah inti practical sesi. Tiga output konkret yang bisa langsung dikerjakan setelah sesi ini.
-->

---
layout: default
---

# Buku Ajar vs Buku Referensi

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

## 📗 Buku Ajar (*Textbook*)
- Ditulis sebagai **pegangan mata kuliah**
- Urutan mengikuti silabus/RPS
- Ada latihan, studi kasus, rangkuman
- Bahasa lebih accessible
- Target: mahasiswa yang belajar

**Contoh judul:**
*"Pemrograman Web: Konsep dan Praktik"*

</div>
<div>

## 📘 Buku Referensi (*Reference Book*)
- Bersifat **komprehensif & mendalam**
- Tidak harus mengikuti urutan silabus
- Lebih akademis / berbasis riset
- Target: akademisi, praktisi, peneliti

**Contoh judul:**
*"Analisis Keamanan Sistem Informasi: Pendekatan Formal"*

</div>
</div>

<div class="mt-4 border-t pt-2 text-sm opacity-70">
  Keduanya <strong>dapat memperoleh ISBN</strong> dari Perpusnas — selama bersifat umum dan disebarluaskan secara luas, bukan hanya untuk kelas tertentu.
</div>

<!--
Kebanyakan dosen akan menulis buku ajar terlebih dahulu karena langsung terhubung dengan RPS.
Buku referensi lebih cocok untuk dosen yang sudah punya riset kuat di bidangnya.
-->

---
layout: default
---

# Workflow Buku Ajar dengan AI

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## ✅ Kunci Sukses

1. **RPS → Peta Bab** (sudah divalidasi)
2. **Glosarium istilah** di awal
3. **Draft per sub-bab** (bukan per bab penuh)
4. **Verifikasi sitasi** sebelum pindah bab
5. **Min. 49 halaman** (syarat ISBN)

</div>
<div>

## ⚠️ Jebakan Umum

- Melewati outlining → struktur berantakan
- Satu sesi tulis banyak bab → kehilangan kontrol
- Lupa verifikasi `[SITASI?]` → referensi palsu
- **Kata Pengantar berisi ucapan terima kasih** → bisa ditolak ISBN

</div>
</div>

<div class="mt-3 border-l-4 border-red-400 pl-4 text-sm">
  ⚠️ <strong>Perpusnas: Kata Pengantar harus mendeskripsikan isi buku</strong>, bukan berisi ucapan terima kasih. Ucapan terima kasih yang mendominasi kata pengantar adalah alasan penolakan yang sering terjadi.
</div>

<!--
Kata Pengantar yang berisi ucapan terima kasih adalah salah satu alasan paling sering buku ditolak ISBN.
Ini adalah hal sepele yang sering diabaikan dan bisa memperlambat proses penerbitan berbulan-bulan.
Lanjutkan ke slide berikut untuk contoh prompt yang langsung menghindari semua jebakan ini.
-->

---
layout: default
class: prompt-lib
---

# Contoh Prompt — Hindari Jebakan Buku Ajar

*Copy-paste langsung. Ganti bagian [dalam kurung kotak] dengan konten Anda.*

```text
[DRAFT ANTI-JEBAKAN]
Kamu penulis buku ajar akademik Indonesia. Konteks proyek: [rps-konteks.md]
Tulis draf Sub-bab [x.y]: "[Judul Sub-bab]".
Aturan wajib:
- Tulis HANYA dari referensi yang saya lampirkan — jangan mengarang fakta atau angka
- Tandai [VERIFIKASI] pada data faktual (statistik, angka, pernyataan spesifik)
- Tandai [SITASI?] pada klaim yang butuh rujukan ilmiah
- Ikuti glosarium & gaya penulisan pada file konteks
- Tulis SATU sub-bab ini saja — jangan lanjut ke sub-bab berikutnya
- Tutup dengan ringkasan 3 poin utama
```

```text
[KATA PENGANTAR LAYAK ISBN]
Tulis Kata Pengantar buku ajar ini.
Fokus pada: (1) apa isi buku, (2) untuk siapa buku ini,
(3) bagaimana struktur bab, (4) cara terbaik menggunakannya.
Maksimal 400 kata. JANGAN diisi ucapan terima kasih —
kata pengantar harus mendeskripsikan isi buku agar lolos verifikasi Perpusnas.
```

<!--
Dua prompt ini langsung menjawab empat jebakan di slide sebelumnya:
1. [VERIFIKASI]/[SITASI?] → cegah halusinasi & sitasi palsu
2. "satu sub-bab saja" → cegah kehilangan kontrol per sesi
3. Kata Pengantar yang deskriptif → cegah penolakan ISBN
Sarankan audiens screenshot slide ini sebelum lanjut.
-->

---
layout: default
---

# Pitfalls Buku Ajar: Tiga Bahaya Utama

<div class="grid grid-cols-3 gap-4 mt-4">

<div class="border rounded-lg p-4 border-red-300">
<h3 class="font-bold text-red-700">1. 🌫️ Halusinasi Fakta</h3>
<p class="text-sm mt-2">AI mengarang fakta, angka, nama tokoh, atau kejadian yang tidak pernah ada.</p>
<p class="text-sm mt-2"><strong>Mitigasi:</strong> Selalu minta AI hanya menulis dari referensi yang Anda berikan. Tandai klaim faktual dengan <code>[VERIFIKASI]</code>.</p>
</div>

<div class="border rounded-lg p-4 border-orange-300">
<h3 class="font-bold text-orange-700">2. 📚 Sitasi Palsu</h3>
<p class="text-sm mt-2">AI mengarang judul artikel, nama jurnal, tahun, volume, halaman, dan DOI yang tidak ada.</p>
<p class="text-sm mt-2"><strong>Mitigasi:</strong> Gunakan <code>[SITASI?]</code> di prompt. Verifikasi SEMUA referensi di Google Scholar / Scopus sebelum submit.</p>
</div>

<div class="border rounded-lg p-4 border-yellow-300">
<h3 class="font-bold text-yellow-700">3. 📋 Keseragaman Palsu</h3>
<p class="text-sm mt-2">Setiap bab terasa memiliki "suara" yang berbeda karena ditulis di sesi terpisah.</p>
<p class="text-sm mt-2"><strong>Mitigasi:</strong> File konteks gaya penulisan + editing pass lintas bab di akhir.</p>
</div>

</div>

<!--
Ini adalah tiga masalah terbesar yang harus diketahui setiap dosen sebelum menggunakan AI untuk menulis buku akademik.
Tekankan bahwa semua masalah ini bisa dimitigasi — bukan alasan untuk tidak menggunakan AI, tapi alasan untuk menggunakannya dengan benar.
-->
