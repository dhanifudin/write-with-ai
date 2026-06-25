---
layout: section
---

# Bagian 2
## RPS sebagai *Source of Truth*

*RPS-First Approach*

<!--
Transisi ke bagian RPS. Tanyakan: "Berapa banyak yang punya RPS di folder komputer tapi tidak pernah jadi buku?"
Bagian ini membalikkan cara berpikir: bukan "tulis buku lalu buat RPS", tapi "dari RPS, lahirkan buku".
-->

---
layout: default
---

# Konsep RPS-First

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

## RPS sebagai *Single Source of Truth*

RPS Anda sudah berisi:
- ✅ **CPL** → Capaian Pembelajaran Lulusan
- ✅ **CPMK** → Capaian Pembelajaran Mata Kuliah
- ✅ **Sub-CPMK** per pertemuan
- ✅ **Materi** 16 minggu terstruktur
- ✅ **Asesmen** & bobot penilaian
- ✅ **Referensi** yang sudah dikurasi

</div>
<div>

## Apa yang Diturunkan dari RPS

```
             RPS
          /   |   \
         ▼    ▼    ▼
      BUKU  SLIDE  RPS
      AJAR  KULIAH FINAL
         \    |   /
          ▼   ▼  ▼
         Sinkron 100%
```

> Satu sumber → tiga deliverable.
> Tidak ada inkonsistensi.

</div>
</div>

<!--
Ini adalah insight utama yang sering terlewat. Dosen sudah punya "blueprint buku" dalam RPS mereka — tapi tidak menyadarinya.
AI agentik membantu mewujudkan blueprint itu menjadi naskah nyata.
-->

---
layout: default
---

# Menyusun / Merapikan RPS dengan AI

**Alur:** CPL → CPMK → Sub-CPMK → Materi → Asesmen → Rubrik

Agent drafts → Dosen memvalidasi terhadap standar prodi & akreditasi

<div class="mt-4 border rounded-lg p-4 bg-blue-50">

**💬 Contoh Prompt:**

```text
Kamu adalah editor kurikulum perguruan tinggi Indonesia.
Dari CPL prodi berikut: [tempel CPL Anda]

Susun RPS mata kuliah "[Nama MK]" untuk 16 pertemuan dengan format:
- CPMK (3-5 poin)
- Sub-CPMK per pertemuan
- Materi pokok per pertemuan
- Metode pembelajaran
- Bobot penilaian & rubrik singkat

Output: tabel markdown.
Tandai dengan [VALIDASI] bagian yang perlu saya cek terhadap standar prodi.
```

</div>

<!--
Tekankan instruksi [VALIDASI] — ini mengajarkan audiens untuk selalu meminta AI menandai hal yang perlu dikonfirmasi manusia.
AI tidak tahu standar akreditasi prodi Anda. Tugasnya men-draft, tugas Anda memvalidasi.
-->

---
layout: default
---

# RPS sebagai *Project Brief* — Konteks Persisten

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

## Masalah Tanpa Project Brief
- Tiap sesi AI "lupa" konteks
- Istilah tidak konsisten antar bab
- Gaya penulisan berubah-ubah
- Harus menjelaskan ulang setiap kali

</div>
<div>

## Solusi: File Konteks RPS

Simpan dalam satu file: `rps-konteks.md`
```
# Konteks Buku: [Nama MK]
- Judul buku target: ...
- Audiens: mahasiswa S1 semester 3
- Gaya: akademik tapi mudah dipahami
- Istilah baku: [glosarium]
- RPS lengkap: [tempel isi RPS]
- Struktur bab: [peta bab]
```
Upload/tempel di awal setiap sesi.

</div>
</div>

<div class="mt-2 border-l-4 border-yellow-400 pl-4 text-sm">
  <strong>💡 Contoh berlabel:</strong> Beberapa AI agentik (seperti yang berbasis CLI dengan file konfigurasi proyek) mendukung <em>persistent project memory</em> — konteks ini dimuat otomatis di setiap sesi, tanpa perlu upload ulang. Fitur ini sangat menghemat waktu untuk proyek buku multi-sesi.
</div>

<!--
Ini adalah pola paling practical yang bisa langsung diterapkan audiens hari ini, bahkan dengan chatbot biasa sekalipun.
"Labeled example": persistent project memory adalah fitur unik beberapa agentic CLI — tapi versi manual (copy-paste file konteks) bisa dilakukan di tool apapun.
-->

---
layout: default
---

# Dari RPS ke Peta Bab

**Langkah:** 16 Pertemuan → Kluster Topik → Struktur Bab Buku

<div class="grid grid-cols-2 gap-6 mt-4">
<div class="text-sm">

**RPS (16 pertemuan):**
```
P1: Pengantar & Sejarah
P2-3: Konsep Dasar A
P4-5: Konsep Dasar B
P6: UTS
P7-9: Implementasi
P10-12: Studi Kasus
P13-15: Topik Lanjut
P16: Review & UAS
```

</div>
<div>

**→ Peta Bab Buku:**
```
Bab 1: Pengantar (P1)
Bab 2: Konsep Dasar (P2-5)
Bab 3: Implementasi (P7-9)
Bab 4: Studi Kasus (P10-12)
Bab 5: Topik Lanjut (P13-15)
Lampiran: Soal Latihan
```

</div>
</div>

<div class="mt-2 border rounded-lg p-3 bg-blue-50 text-sm">

**💬 Contoh Prompt:** `"Dari RPS terlampir, usulkan struktur bab buku ajar yang memetakan 16 pertemuan ke bab/sub-bab logis. Jangan tulis isi dulu — beri outline + alasan urutan dan pengelompokan."`

</div>

<!--
Tekankan: jangan langsung minta AI menulis isi buku. Mulai dari outline dulu — lebih mudah dikoreksi, lebih hemat waktu.
Prinsip: validasi struktur sebelum mengisi konten.
-->
