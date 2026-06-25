---
layout: section
---

# Bagian 4
## Teknik Prompt & Context

*Cara Bicara ke AI Agentik*

<!--
Bagian ini mengajarkan teknik prompting yang dapat langsung diterapkan. Tekankan: kualitas output AI sangat bergantung pada kualitas input (prompt) yang diberikan.
"Garbage in, garbage out" berlaku di sini.
-->

---
layout: default
---

# *Context is King*

**Apa yang Anda beri ke AI = batas maksimal kualitas outputnya**

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## ❌ Prompt Miskin Konteks
```text
"Tulis bab tentang jaringan komputer."
```

**Hasilnya:** Generik, tidak sesuai level
mahasiswa, tidak cocok dengan RPS,
istilah tidak konsisten.

</div>
<div>

## ✅ Prompt Kaya Konteks
```text
"Tulis Bab 2 tentang jaringan komputer
untuk buku ajar MK Jaringan Komputer,
program studi Informatika S1 semester 3.
Gaya: akademik tapi mudah dipahami.
Glosarium: [lampiran].
RPS acuan: [lampiran].
Outline bab: [lampiran]."
```

</div>
</div>

<div class="mt-4 text-center text-sm opacity-70">
  📌 Selalu mulai sesi dengan <strong>mengirim file konteks RPS</strong> sebelum meminta AI mengerjakan apapun.
</div>

<!--
Demo langsung kalau memungkinkan: tunjukkan perbedaan output antara prompt miskin dan kaya konteks untuk topik yang sama.
Pesan utama: AI tidak bisa "menebak" apa yang Anda inginkan — Anda harus memberitahukannya secara eksplisit.
-->

---
layout: default
---

# Struktur Prompt: Formula RTCE

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

| Komponen | Isi | Contoh |
|---|---|---|
| **R**ole | Peran AI | "Kamu editor buku ajar akademik Indonesia" |
| **T**ask | Tugas spesifik | "Tulis Sub-bab 2.3 tentang OSI Layer" |
| **C**onstraints | Batasan & format | "Gaya akademik, maks 800 kata, pakai contoh nyata" |
| **E**xamples | Contoh output | "Format seperti sub-bab 1.2 yang sudah disetujui" |

</div>
<div>

**Prompt Lengkap:**
```text
[R] Kamu editor buku ajar akademik
    perguruan tinggi Indonesia.

[T] Tulis Sub-bab 2.3: OSI Layer
    sesuai outline yang sudah
    disetujui.

[C] Gaya: akademik tapi mudah
    dipahami mahasiswa S1.
    Maks 800 kata. Gunakan tabel
    untuk 7 layer OSI.
    Tandai [SITASI?] bila perlu
    referensi.

[E] Ikuti gaya penulisan Sub-bab
    1.2 yang sudah disetujui.
```

</div>
</div>

<!--
Formula RTCE adalah alat bantu yang bisa langsung digunakan audiens hari ini.
Tekankan komponen C (Constraints) — ini yang paling sering dilupakan dan paling mempengaruhi kualitas output.
-->

---
layout: default
---

# Iterative Refinement

**Satu prompt jarang langsung sempurna — dan itu normal.**

<div class="grid grid-cols-3 gap-4 mt-6">

<div class="border rounded-lg p-4 bg-green-50">
<h3 class="font-bold">1. Draft Awal</h3>
<p class="text-sm mt-2">Minta AI membuat draf pertama. Fokus pada struktur & kelengkapan, bukan kesempurnaan.</p>
<p class="text-sm mt-2 italic">"Tulis draf pertama Sub-bab 3.1..."</p>
</div>

<div class="border rounded-lg p-4 bg-yellow-50">
<h3 class="font-bold">2. Critique & Alter</h3>
<p class="text-sm mt-2">Minta AI mengevaluasi draf sendiri, atau berikan feedback spesifik.</p>
<p class="text-sm mt-2 italic">"Bagian mana yang kurang jelas? Usulkan 2 alternatif untuk paragraf pembuka."</p>
</div>

<div class="border rounded-lg p-4 bg-blue-50">
<h3 class="font-bold">3. Finalize</h3>
<p class="text-sm mt-2">Pilih versi terbaik, minta perbaikan spesifik, lalu Anda lakukan sentuhan akhir.</p>
<p class="text-sm mt-2 italic">"Gunakan alternatif B, perkuat dengan contoh dari dunia industri."</p>
</div>

</div>

<!--
Iterative refinement adalah cara kerja yang natural — persis seperti proses revisi buku konvensional.
Bedanya: dengan AI, siklus revisi bisa selesai dalam menit, bukan minggu.
-->

---
layout: default
---

# Mode Kerja Agen: *Plan* dulu, *Execute* kemudian

<div class="grid grid-cols-2 gap-6 mt-4 text-sm">
<div class="border rounded-lg p-4 bg-blue-50">

## 🧭 Plan Mode

Agent **merencanakan & menganalisis** — tidak menulis apapun sampai Anda setuju.

**Gunakan untuk:**
- Membuat peta bab dari RPS
- Merancang outline buku
- Mengusulkan struktur konten baru
- Menganalisis kekurangan draft

**Prinsip:** *Rencanakan → setujui → baru eksekusi.*
Anda menghindari pekerjaan yang harus dibuang.

</div>
<div class="border rounded-lg p-4 bg-green-50">

## ⚡ Execute / Auto Mode

Agent **langsung mengerjakan** — menulis file, mengedit, menghasilkan konten.

**Gunakan untuk:**
- Menulis draf sub-bab yang sudah dioutline
- Menyeragamkan istilah lintas bab
- Generate slide dari bab yang sudah disetujui
- Tugas berulang yang risikonya rendah

**Prinsip:** *Tetap verifikasi output* — terutama fakta & referensi.

</div>
</div>

<div class="mt-3 border-l-4 border-yellow-400 pl-4 text-sm">
  <strong>💡 Contoh berlabel:</strong> <strong>Claude Code</strong> dan <strong>opencode</strong> mendukung <em>Plan Mode</em> (toggle dengan <kbd>Shift+Tab</kbd> atau flag <code>--plan</code>). Dalam Plan Mode, agent tidak mengubah file apapun — hanya mengusulkan langkah. Sangat aman untuk sesi pemetaan bab dari RPS.
</div>

<!--
Analogi: Plan Mode = rapat desain bersama arsitek sebelum mulai membangun.
Execute Mode = kontraktor yang sudah punya blueprint yang disetujui.
Dosen sebagai director: gunakan Plan Mode untuk semua keputusan struktural, Execute untuk tugas drafting yang sudah jelas.
-->

---
layout: default
---

# Proyek Panjang: Memory, Chunking & Continuity

**Buku bukan sprint — ini maraton. AI agentik dirancang untuk itu.**

<div class="grid grid-cols-3 gap-4 mt-6">

<div class="border rounded-lg p-4">
<h3 class="font-bold text-sm">🧠 Memory Files</h3>
<p class="text-sm mt-2">Simpan: RPS, glosarium, outline, gaya penulisan, progress. Bawa di setiap sesi baru.</p>
<p class="text-sm mt-1 font-mono bg-gray-100 p-1">rps-konteks.md<br>glosarium.md<br>progress.md</p>
</div>

<div class="border rounded-lg p-4">
<h3 class="font-bold text-sm">✂️ Chunking</h3>
<p class="text-sm mt-2">Jangan tulis seluruh bab sekaligus. Pecah per sub-bab. Lebih mudah dikontrol dan divalidasi.</p>
<p class="text-sm mt-1">Satu sesi = satu sub-bab ✅<br>Satu sesi = satu bab penuh ⚠️</p>
</div>

<div class="border rounded-lg p-4">
<h3 class="font-bold text-sm">🔗 Continuity</h3>
<p class="text-sm mt-2">Mulai sesi baru dengan recap:</p>
<p class="text-sm mt-1 font-mono bg-gray-100 p-1">"Sesi lalu kita selesaikan<br>Sub-bab 2.3. Sekarang<br>lanjut ke 2.4 tentang [X].<br>File konteks terlampir."</p>
</div>

</div>

<!--
Proyek buku bisa berlangsung berminggu-minggu. Tekankan pentingnya "memory files" — ini adalah investasi di awal yang menghemat banyak waktu di tengah dan akhir proyek.
-->
