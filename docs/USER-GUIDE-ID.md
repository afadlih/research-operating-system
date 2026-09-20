# Panduan Pengguna (Bahasa Indonesia)

Panduan lengkap untuk menyiapkan dan menggunakan Research Operating System di platform AI Anda.

---

## Yang Anda Butuhkan

- Akun platform AI (ChatGPT, Gemini, Claude, atau NotebookLM)
- File Research Operating System (dari repository ini)
- Topik atau materi penelitian Anda

Tidak memerlukan kemampuan coding untuk alur kerja penelitian standar.

---

## Panduan Cepat (5 Langkah)

### 1. Unduh atau Clone Repository Ini

Unduh repository ini sebagai file ZIP, atau gunakan Git:

```bash
git clone https://github.com/afadlih/research-operating-system.git
```

### 2. Pilih Platform AI Anda

Lihat [Platform Usage Map](PLATFORM-USAGE-MAP.md) untuk panduan operasional tiap platform.

- **Rekomendasi untuk alur kerja penuh:** ChatGPT Projects atau Claude Projects (menyediakan konteks proyek persisten melalui project chats, files, dan instructions).
- **Rekomendasi untuk ekstraksi literatur:** NotebookLM.
- **Rekomendasi untuk penelitian komputasi:** Coding agent (Cursor, Windsurf, Claude Code) menggunakan file instruksi bawaan platform (`AGENTS.md` atau `CLAUDE.md`).

### 3. Salin File Protokol ke Proyek Penelitian Anda

Buat folder proyek penelitian Anda dan salin direktori protokol:

```
my-research-project/
|-- AGENTS.md                 # Opsional: disesuaikan untuk coding agent yang didukung
|-- PROJECT-CONTEXT.md        # Dibuat dari 09-project-context-template.md
|-- research-protocol/        # Disalin dari repo Research OS
|   |-- RESEARCH.md
|   |-- 00-RESEARCH-CORE.md
|   \-- [modul-aktif].md
\-- literature/               # Paper PDF, catatan, dan draft Anda
```

**Yang disalin dari Research OS:**
- Folder `research-protocol/` berisi `RESEARCH.md`, `00-RESEARCH-CORE.md`, dan modul aktif.
- `09-project-context-template.md` (isi dan simpan sebagai `PROJECT-CONTEXT.md`).
- `AGENTS.md` (opsional - hanya jika coding agent Anda mendukungnya; selain itu gunakan konvensi platform seperti `CLAUDE.md`).

**Yang dibuat sendiri oleh peneliti:**
- `PROJECT-CONTEXT.md` (berisi topik, pertanyaan penelitian, batasan, dan parameter studi).
- Dokumen literatur asli (PDF, catatan sintesis), dataset, instrumen, dan naskah bab.

### 4. Upload Core + Modul Sesuai Tahap

Setiap sesi memerlukan:
1. `research-protocol/RESEARCH.md` - router utama
2. `research-protocol/00-RESEARCH-CORE.md` - aturan integritas universal

Tambahkan modul yang sesuai dengan tahap Anda dalam Siklus Penelitian Kanonikal:

| Tahap Siklus Penelitian | File yang Diupload |
|---|---|
| Perumusan Masalah (Problem) | `03-research-literature.md` |
| Tinjauan Pustaka (Evidence / Literature) | `03-research-literature.md` + `01-research-writing.md` |
| Kesenjangan Penelitian (Research Gap) | `03-research-literature.md` + `04-research-methodology.md` |
| Pertanyaan Penelitian (Research Question) | `04-research-methodology.md` |
| Desain Metodologi (Methodology) | `04-research-methodology.md` (+ `02-research-human.md` jika subjek manusia) |
| Pengumpulan Data / Eksperimen (Data / Experiment) | `04-research-methodology.md` + `05-research-experiment.md` |
| Analisis Statistik (Analysis) | `06-research-analysis.md` + `05-research-experiment.md` |
| Penulisan Naskah & Kesimpulan (Writing & Conclusion) | Modul aktif + `01-research-writing.md` |
| Audit Akhir (Audit) | `07-research-audit.md` + semua modul yang digunakan |

*(Catatan untuk ChatGPT obrolan biasa: RESEARCH.md dapat dihilangkan hanya jika pengguna memilih modul yang tepat secara manual dan tidak memerlukan fungsi router. Rekomendasi default untuk pemula adalah menyertakan RESEARCH.md.)*

### 5. Mulai dengan Prompt Terstruktur

Gunakan Pustaka Prompt ([Indonesia](../prompts/PROMPT-LIBRARY-ID.md) | [English](../prompts/PROMPT-LIBRARY-EN.md)) atau gunakan prompt pembuka berikut:

```
Saya memulai penelitian menggunakan Research Operating System.
Saya telah mengupload RESEARCH.md dan 00-RESEARCH-CORE.md.
Topik penelitian saya: [Tuliskan Topik Anda].
Bantu saya merumuskan:
- rumusan masalah
- bukti empiris yang dibutuhkan
- kelayakan metodologis
Jangan langsung menulis draf naskah. Mulai dari klarifikasi bukti dan pertanyaan penelitian.
```

---

## Siklus Penelitian Kanonikal

Ikuti urutan progresif ini selama penelitian berlangsung:

```
Problem (Rumusan Masalah)
  -> Evidence / Literature (Bukti / Literatur)
    -> Research Gap (Kesenjangan Penelitian)
      -> Research Question (Pertanyaan Penelitian)
        -> Methodology (Desain Metodologi)
          -> Data / Experiment (Data / Eksperimen)
            -> Analysis (Analisis Hasil)
              -> Writing & Conclusion (Penulisan & Kesimpulan)
                -> Audit (Audit Akhir)
```

**Jangan melompati tahap.** Setiap tahap dibangun di atas verifikasi dari tahap sebelumnya.

---

## Hal yang Boleh dan Tidak Boleh Dilakukan

### Boleh (DO)

- Selalu sertakan `00-RESEARCH-CORE.md` di setiap sesi.
- Upload hanya modul yang dibutuhkan untuk tahap yang sedang dikerjakan.
- Isi `PROJECT-CONTEXT.md` agar AI memahami batasan dan konteks studi Anda.
- Verifikasi setiap sitasi dan klaim langsung ke paper aslinya.
- Lakukan audit akhir (`07-research-audit.md`) sebelum menganggap pekerjaan selesai.

### Tidak Boleh (DO NOT)

- Mengupload semua 14 file sekaligus tanpa tujuan yang jelas.
- Langsung meminta AI menulis bab tanpa merumuskan metodologi dan bukti.
- Menerima mentah-mentah hasil AI tanpa memverifikasi data dan sumber.
- Membiarkan AI mengarang sitasi, judul artikel, atau angka statistik.
- Menganggap saran AI sebagai fakta ilmiah sebelum diverifikasi secara mandiri.

---

## Penafian Integritas Akademik (Disclaimer)

Research OS mendukung kualitas dan integritas riset; **namun tidak menjaminnya secara otomatis**.
Framework ini tidak menjamin penerimaan skripsi/tesis, publikasi jurnal, metodologi tanpa cacat, atau skor AI detector tertentu. Framework ini menyediakan panduan verifikasi (*verification-first*) agar peneliti dapat mempertahankan standar akademik yang dapat dipertanggungjawabkan.

---

## Kesalahan Umum

| Kesalahan | Dampak | Solusi yang Benar |
|---|---|---|
| Upload seluruh 14 file sekaligus | Konteks AI penuh dan AI mengabaikan instruksi penting | Upload hanya `CORE` + `RESEARCH.md` + 1 modul aktif |
| Meminta AI langsung menulis bab skripsi | Teks menjadi generik, dangkal, dan penuh sitasi halusinasi | Selesaikan tahap masalah, literatur, dan metode dulu |
| Mengandalkan sitasi dari AI | AI bisa mengarang nama penulis, tahun, dan DOI | Upload PDF asli atau cari langsung di Scopus / Google Scholar |
| Memakai `AGENTS.md` di ChatGPT web | Menambah instruksi coding yang tidak relevan untuk obrolan web | Gunakan `RESEARCH.md` + `CORE` untuk web |
| Melewatkan tahap audit | Celah metodologis atau variabel pengganggu tidak terdeteksi | Jalankan `07-research-audit.md` sebelum sidang/submit |

---

## Langkah Selanjutnya

- [START-HERE.md](../START-HERE.md) - panduan onboarding singkat
- [Platform Usage Map](PLATFORM-USAGE-MAP.md) - panduan operasional tiap platform
- [File Function Map](FILE-FUNCTION-MAP.md) - daftar lengkap fungsi setiap file
- [Pustaka Prompt (ID)](../prompts/PROMPT-LIBRARY-ID.md) - 16 template prompt siap pakai
- [RESEARCH.md](../research-protocol/RESEARCH.md) - router utama dengan tabel routing lengkap
