# Pustaka Prompt (Bahasa Indonesia)

Kumpulan prompt siap pakai untuk Research Operating System. Salin dan tempel ke platform AI Anda setelah mengupload file protocol yang diperlukan.

---

## Memulai Penelitian

### Mulai Proyek Penelitian Baru

> **Modul yang diperlukan:** CORE

```
Saya memulai proyek penelitian.

Gunakan Research Operating System.

Bantu saya mendefinisikan:
- rumusan masalah
- bukti yang diperlukan
- penilaian kelayakan
- potensi pertanyaan penelitian

Jangan langsung ke tahap penulisan.
Jangan membuat sumber atau sitasi palsu.
```

### Muat Konteks Proyek

> **Modul yang diperlukan:** CORE + PROJECT-CONTEXT

```
Berikut konteks proyek saya: [tempel atau upload 09-project-context-template.md]

Tinjau keadaan penelitian saya saat ini.
Identifikasi apa yang sudah selesai dan apa yang masih tersisa.
Tandai ketidakkonsistenan antara metodologi yang dinyatakan dan progres saat ini.
```

---

## Review Literatur

### Analisis Paper

> **Modul yang diperlukan:** CORE + LITERATURE

```
Analisis paper-paper berikut.

Ekstrak untuk setiap paper:
- tujuan penelitian
- metodologi yang digunakan
- temuan utama
- keterbatasan yang dinyatakan penulis
- keterbatasan yang perlu saya catat
- kemungkinan kontribusi terhadap research gap

Pisahkan fakta dari sumber dan interpretasi Anda.
Tandai hal yang tidak pasti sebagai [INTERPRETASI].
```

### Bangun Matriks Bukti

> **Modul yang diperlukan:** CORE + LITERATURE

```
Berdasarkan paper yang saya berikan, bangun matriks bukti (evidence matrix).

Kolom:
- Penulis dan Tahun
- Pertanyaan/Tujuan Penelitian
- Metode
- Temuan Utama
- Keterbatasan
- Relevansi dengan penelitian saya

Jangan menambahkan paper yang tidak saya berikan.
Jangan memalsukan penulis, tahun, atau temuan.
```

### Identifikasi Research Gap

> **Modul yang diperlukan:** CORE + LITERATURE + METHODOLOGY

```
Berdasarkan literatur yang sudah saya review, bantu identifikasi research gap.

Persyaratan:
- Gap harus muncul dari bukti yang sudah ditinjau.
- Tunjukkan studi mana yang mendukung klaim gap tersebut.
- Jelaskan mengapa gap ini penting.
- Nilai apakah gap ini dapat diatasi dalam lingkup studi saya.

Jangan mengklaim "belum ada penelitian" kecuali terverifikasi.
```

### Strategi Pencarian Sistematis

> **Modul yang diperlukan:** CORE + LITERATURE

```
Bantu saya merancang strategi pencarian literatur sistematis.

Topik penelitian: [topik Anda]

Definisikan:
- kata kunci pencarian dan kombinasi Boolean
- database target (Scopus, WoS, IEEE, ACM, dll.)
- kriteria inklusi
- kriteria eksklusi
- justifikasi rentang tahun
- kriteria penilaian kualitas

Ikuti panduan PRISMA jika berlaku.
```

---

## Metodologi

### Rancang Metodologi Penelitian

> **Modul yang diperlukan:** CORE + METHODOLOGY

```
Bantu saya merancang metodologi penelitian.

Pertanyaan penelitian: [RQ Anda]

Definisikan:
- jenis dan justifikasi desain penelitian
- variabel (independen, dependen, kontrol)
- definisi operasional
- populasi dan strategi sampling
- metode pengumpulan data
- rencana validitas dan reliabilitas
- ancaman terhadap validitas

Metode harus mampu menjawab pertanyaan penelitian.
Jangan menyarankan metode tanpa justifikasi.
```

### Desain Kuesioner / Survei

> **Modul yang diperlukan:** CORE + METHODOLOGY + HUMAN

```
Bantu saya merancang kuesioner penelitian.

Variabel penelitian: [variabel Anda]
Target responden: [deskripsi]

Persyaratan:
- item harus sesuai dengan definisi operasional
- gunakan skala tervalidasi jika ada
- jelaskan pilihan skala Likert atau pengukuran
- jelaskan rencana validitas isi
- jelaskan rencana uji reliabilitas (misal: threshold Cronbach's alpha)

Jangan membuat item yang tidak dapat ditelusuri ke variabel penelitian.
```

### Strategi Sampling

> **Modul yang diperlukan:** CORE + METHODOLOGY

```
Bantu saya menentukan strategi sampling dan ukuran sampel.

Populasi: [deskripsi]
Desain penelitian: [desain Anda]

Jelaskan:
- teknik sampling dan justifikasi
- perhitungan atau aturan ukuran sampel
- kriteria inklusi/eksklusi
- potensi bias sampling
- batasan generalisasi
```

---

## Eksperimen

### Rancang Protokol Eksperimen

> **Modul yang diperlukan:** CORE + METHODOLOGY + EXPERIMENT

```
Bantu saya merancang protokol eksperimen.

Konteks penelitian: [konteks Anda]

Definisikan:
- deskripsi dan sumber dataset
- strategi pembagian train/validation/test
- model atau metode baseline
- metode yang diajukan
- metrik evaluasi dan justifikasi
- strategi hyperparameter tuning
- random seed dan rencana reprodusibilitas
- jumlah pengulangan
- checklist pencegahan kebocoran data

Jangan mengklaim hasil sebelum eksperimen dijalankan.
```

### Cek Kebocoran Data Eksperimen

> **Modul yang diperlukan:** CORE + EXPERIMENT

```
Tinjau desain eksperimen saya untuk potensi kebocoran data.

Periksa:
- Apakah data test digunakan saat training atau tuning?
- Apakah feature engineering diterapkan sebelum pembagian data?
- Apakah ada kebocoran temporal atau kelompok?
- Apakah metrik evaluasi dihitung pada split yang benar?
- Apakah hyperparameter dipilih berdasarkan performa test?

Laporkan setiap masalah dengan tingkat keparahan (CRITICAL / MAJOR / MINOR).
```

---

## Analisis

### Interpretasi Hasil Eksperimen

> **Modul yang diperlukan:** CORE + ANALYSIS

```
Berikut hasil eksperimen saya: [tempel hasil]

Analisis:
- statistik deskriptif
- perbandingan performa antar metode
- signifikansi statistik (jika berlaku)
- effect size dan signifikansi praktis
- confidence interval atau ketidakpastian
- analisis error

Jaga kesimpulan tetap dalam batas yang didukung bukti.
Jangan overclaiming. Nyatakan keterbatasan dengan jelas.
```

### Pemilihan Uji Statistik

> **Modul yang diperlukan:** CORE + ANALYSIS

```
Bantu saya memilih uji statistik yang tepat.

Karakteristik data:
- ukuran sampel: [N]
- jumlah kelompok: [N]
- jenis data: [kontinu/ordinal/nominal]
- distribusi: [normal/non-normal/tidak diketahui]
- desain: [independen/berpasangan/pengukuran berulang]

Rekomendasikan uji yang tepat, nyatakan asumsi, dan jelaskan makna hasilnya.
```

---

## Penulisan

### Tulis Bagian Tinjauan Pustaka

> **Modul yang diperlukan:** CORE + LITERATURE + WRITING

```
Bantu saya menulis bagian tinjauan pustaka.

Berdasarkan paper dan matriks bukti yang sudah saya berikan:
- sintesis temuan (jangan hanya daftar paper)
- bangun argumen logis menuju research gap
- jaga konsistensi terminologi
- bedakan fakta sumber dari interpretasi
- gunakan kekuatan klaim yang terkalibrasi

Jangan menambahkan sitasi yang tidak saya berikan.
Jangan gunakan pengisi akademik yang generik.
```

### Tulis Bagian Metodologi

> **Modul yang diperlukan:** CORE + METHODOLOGY + WRITING

```
Bantu saya menulis bagian metodologi berdasarkan desain penelitian saya.

Sertakan:
- gambaran desain penelitian
- populasi dan sampling
- variabel dan definisi operasional
- prosedur pengumpulan data
- rencana analisis data
- validitas dan reliabilitas

Tulis dalam prosa akademik yang jelas.
Jangan mengarang detail metodologis yang belum saya definisikan.
```

### Tulis Hasil dan Pembahasan

> **Modul yang diperlukan:** CORE + ANALYSIS + WRITING

```
Bantu saya menulis bagian hasil dan pembahasan.

Berdasarkan hasil eksperimen aktual saya:
- sajikan hasil dengan jelas menggunakan tabel/gambar yang sesuai
- bandingkan dengan baseline dan penelitian sebelumnya
- diskusikan implikasi
- nyatakan keterbatasan dengan jujur
- jaga pembahasan proporsional terhadap bukti

Jangan mengklaim hasil yang tidak diproduksi.
Jangan memperkuat kesimpulan melampaui data.
```

---

## Audit dan Review

### Mode Reviewer Kritis

> **Modul yang diperlukan:** CORE + modul relevan

```
Bertindak sebagai reviewer penelitian yang kritis.

Tinjau [bab/bagian/desain] saya dan identifikasi:
- asumsi yang tidak didukung
- kelemahan metodologis
- bukti yang hilang
- overclaiming
- celah verifikasi

Untuk setiap masalah, nyatakan:
- apa yang salah
- mengapa itu penting
- apa yang harus diubah
- bagaimana memverifikasi koreksinya

Jangan membuat kritik tanpa dasar.
Jika karya sudah kuat, katakan demikian.
```

### Audit Penelitian Lengkap

> **Modul yang diperlukan:** CORE + SEMUA modul yang digunakan + AUDIT

```
Lakukan audit penelitian lengkap menggunakan 07-research-audit.md.

Periksa keselarasan antara:
- pertanyaan penelitian dan metode
- metode dan eksperimen
- eksperimen dan analisis
- analisis dan kesimpulan
- literatur dan research gap
- tulisan dan bukti

Untuk setiap area, laporkan PASS atau FAIL dengan bukti.
Status akhir harus: READY / READY WITH LIMITATIONS / NOT READY.
```

### Review Bagian Latar Belakang

> **Modul yang diperlukan:** CORE + LITERATURE + WRITING + BACKGROUND-GENERATOR

```
Tinjau bagian latar belakang penelitian saya menggunakan 11-research-background-generator.md.

Periksa:
- Apakah masalah didefinisikan dengan jelas dan didukung bukti?
- Apakah klaim didukung sitasi?
- Apakah penelitian sebelumnya disintesis (bukan hanya didaftar)?
- Apakah research gap berbasis bukti?
- Apakah tujuan mengikuti dari gap?
- Apakah ada pengisi generik yang harus diganti?

Gunakan format audit B-XX untuk setiap temuan.
```

---

## Adaptasi Domain

### Sesuaikan untuk Domain Penelitian Saya

> **Modul yang diperlukan:** CORE + DOMAIN-ADAPTATION

```
Saya melakukan penelitian di bidang [domain Anda].

Gunakan 10-research-domain-adaptation.md.

Pilih modul yang relevan untuk domain saya.

Topik penelitian: [topik Anda]
Tugas saat ini: [tugas Anda]

Periksa:
- kesesuaian metodologis untuk domain ini
- persyaratan bukti khusus domain
- risiko umum yang harus dihindari di bidang ini
```

---

## Tips Penggunaan Prompt

1. **Ganti teks dalam kurung siku** `[seperti ini]` dengan informasi Anda.
2. **Upload modul yang diperlukan** yang tercantum di atas setiap prompt sebelum menggunakannya.
3. **Kombinasikan prompt** sesuai kebutuhan - mulai dari perencanaan, lalu metodologi, lalu eksperimen, dst.
4. **Jangan gunakan semua prompt sekaligus.** Ikuti urutan lifecycle penelitian.
5. **Verifikasi output AI** terhadap sumber dan data aktual Anda.
