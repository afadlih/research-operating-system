# Panduan Pengguna (Bahasa Indonesia)

Panduan lengkap untuk menyiapkan dan menggunakan Research Operating System di platform AI Anda.

---

## Yang Anda Butuhkan

- Akun platform AI (ChatGPT, Gemini, Claude, atau NotebookLM)
- File Research Operating System (repository ini)
- Topik atau materi penelitian Anda

Tidak perlu kemampuan coding.

---

## Langkah-Langkah Setup

### 1. Download Repository Ini

Klik tombol hijau **Code** di GitHub dan pilih **Download ZIP**, atau clone:

```bash
git clone https://github.com/afadlih/research-operating-system.git
```

### 2. Pilih Platform AI

Lihat [Platform Usage Map](PLATFORM-USAGE-MAP.md) untuk instruksi per platform.

**Rekomendasi:** ChatGPT Projects untuk workflow penuh.

### 3. Upload File Inti

Setiap tugas penelitian minimal membutuhkan:

1. `research-protocol/RESEARCH.md` — router utama
2. `research-protocol/00-RESEARCH-CORE.md` — aturan integritas penelitian universal

### 4. Upload Modul Sesuai Tugas

Berdasarkan tugas Anda saat ini, tambahkan modul yang relevan:

| Tugas Anda | Upload Modul Ini |
|---|---|
| Mencari topik penelitian | `03-research-literature.md` |
| Review literatur | `03-research-literature.md` + `01-research-writing.md` |
| Merumuskan research question | `04-research-methodology.md` |
| Desain metodologi | `04-research-methodology.md` (+ `02-research-human.md` jika melibatkan manusia) |
| Menjalankan eksperimen | `04-research-methodology.md` + `05-research-experiment.md` |
| Analisis hasil | `06-research-analysis.md` + `05-research-experiment.md` |
| Menulis bab | Modul relevan + `01-research-writing.md` |
| Audit akhir | `07-research-audit.md` + semua modul yang digunakan |

### 5. Mulai dengan Prompt

Gunakan Prompt Library ([English](../prompts/PROMPT-LIBRARY-EN.md) | [Indonesia](../prompts/PROMPT-LIBRARY-ID.md)) untuk prompt siap pakai, atau sampaikan ke AI:

```
Saya memulai proyek penelitian.
Gunakan Research Operating System.
Bantu saya mendefinisikan:
- masalah penelitian
- bukti yang diperlukan
- kelayakan
Jangan langsung ke tahap penulisan.
```

---

## Alur Kerja Penelitian

Ikuti urutan umum berikut:

```
Masalah → Pertanyaan Penelitian → Bukti Literatur → Metodologi
→ Pengumpulan Data → Eksperimen → Analisis → Penulisan → Audit Akhir
```

**Jangan melompati tahapan.** Setiap tahap dibangun dari tahap sebelumnya.

---

## Setup Per Platform

### ChatGPT Projects (Rekomendasi)

1. Buat Project baru di ChatGPT.
2. Upload file berikut ke Project:
   - `research-protocol/AGENTS.md`
   - `research-protocol/RESEARCH.md`
   - `research-protocol/00-RESEARCH-CORE.md`
   - Modul yang Anda butuhkan
3. Set instruksi Project:

```
Gunakan RESEARCH.md sebagai router.
Gunakan modul sesuai kebutuhan.
Jangan membuat evidence, citation, atau hasil yang tidak diverifikasi.
```

### ChatGPT Chat Biasa

1. Buka chat baru.
2. Lampirkan:
   - `RESEARCH.md`
   - `00-RESEARCH-CORE.md`
   - Modul sesuai tugas
3. Sampaikan tugas Anda.

### Gemini Gems

1. Buat Gem baru.
2. Upload file protocol sebagai knowledge.
3. Set instruksi Gem merujuk ke `RESEARCH.md`.

### Claude Projects

1. Buat Project baru.
2. Tambahkan file protocol ke Project Knowledge.
3. Atau buat `CLAUDE.md` dengan pointer ke research protocol.

### NotebookLM

1. Buat Notebook baru.
2. Upload paper penelitian sebagai sumber.
3. Upload `03-research-literature.md` untuk panduan analisis literatur.
4. Gunakan terutama untuk literature review dan evidence extraction.

---

## Yang Boleh dan Tidak Boleh

### BOLEH

- Selalu load `00-RESEARCH-CORE.md` untuk setiap tugas
- Load hanya modul yang dibutuhkan saat ini
- Ikuti task routing table di RESEARCH.md
- Verifikasi klaim dengan bukti sebelum menerimanya
- Jalankan audit akhir sebelum menyatakan selesai

### TIDAK BOLEH

- Upload semua file sekaligus tanpa tujuan
- Langsung loncat dari definisi masalah ke penulisan
- Terima output AI tanpa cek bukti
- Biarkan AI membuat sitasi atau hasil palsu
- Perlakukan saran AI sebagai fakta terverifikasi

---

## Kesalahan Umum

| Kesalahan | Mengapa Bermasalah | Yang Harus Dilakukan |
|---|---|---|
| Upload 14 file sekaligus | Membingungkan AI, boros konteks | Upload hanya sesuai kebutuhan tugas |
| Skip review literatur | Research gap tanpa dasar bukti | Bangun bukti dulu, baru identifikasi gap |
| Terima sitasi dari AI tanpa cek | AI bisa memalsukan penulis, DOI, tanggal | Verifikasi setiap sitasi ke sumber asli |
| Menulis sebelum metodologi solid | Tulisan harus ditulis ulang total | Desain metodologi dulu, tulis kemudian |
| Skip audit akhir | Masalah integritas tidak terdeteksi | Selalu jalankan `07-research-audit.md` |

---

## Dukungan Multi-Domain

Sistem ini mendukung 10+ bidang penelitian:

- Ilmu Komputer / AI
- Teknik
- Pendidikan
- Psikologi
- Kesehatan / Kedokteran
- Bisnis / Manajemen
- Ekonomi
- Ilmu Sosial
- Hukum
- Humaniora

Lihat [10-research-domain-adaptation.md](../research-protocol/10-research-domain-adaptation.md) untuk panduan per domain.

---

## Butuh Bantuan?

- [File Function Map](FILE-FUNCTION-MAP.md) — fungsi setiap file
- [Platform Usage Map](PLATFORM-USAGE-MAP.md) — detail setup per platform
- [Prompt Library (EN)](../prompts/PROMPT-LIBRARY-EN.md) — ready-to-use prompts
- [Pustaka Prompt (ID)](../prompts/PROMPT-LIBRARY-ID.md) — prompt siap pakai
- [RESEARCH.md](../research-protocol/RESEARCH.md) — router utama dengan tabel routing lengkap
