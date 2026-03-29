# Laporan Penilaian Tugas Terstruktur — Minggu 1-4
**Kelompok:** cc-kelompok-stranger_things
**Mata Kuliah:** Komputasi Awan (SI2514027)
**Periode:** Minggu 1–4 (24 Feb – 22 Mar 2026)
**Penilai:** Aidil Saputra Kirsan, S.ST., M.Tr.Kom.
**Tanggal Penilaian:** 29 Maret 2026
**Referensi RPS:** Sub-CPMK-1 — Aplikasi full-stack berbasis REST API dengan pengelolaan konfigurasi yang baik

---

## A. Identitas Kelompok

| Nama | NIM | Peran |
|------|-----|-------|
| Ahmad Daffa Alfattah | 10231008 | Lead Backend |
| Nazwa Amelia Zahra | 10231068 | Lead Frontend |
| Verina Rahma Dinah | 10231090 | Lead QA & Docs |
| Cintya Widhi Astuti | 10231026 | Lead DevOps |

**Nama Proyek:** Bye Bye Virus (Child Immunization & Growth Tracker)
**Repo:** cc-kelompok-stranger_things

---

## B. Rekap Kontribusi Git (TERVERIFIKASI dari `git log`)

### Jumlah Commit per Anggota per Minggu

| Anggota | Minggu 1 (W9) | Minggu 2 (W10) | Minggu 3 (W11) | Minggu 4 (W12) | Total |
|---------|:---:|:---:|:---:|:---:|:---:|
| Ahmad Daffa | 6 | 3 | 4 | 4 | **17** |
| Nazwa Amelia | 8 | 3 | 3 | 2 | **16** |
| Verina Rahma | 5 | 5 | 2 | 3 | **15** |
| Cintya Widhi | 2 | 1 | 1 | 2 | **6** |

> Catatan: Semua anggota memiliki commit setiap minggu ✅

### File yang Disentuh per Anggota (TERVERIFIKASI dari `git log --name-only`)

| Anggota | Area Kerja Utama | File Kunci |
|---------|-----------------|-----------|
| Daffa | Backend logic & auth | `backend/main.py` (8×), `auth.py`, `crud.py`, `schemas.py`, `models.py` |
| Nazwa | Frontend React | `frontend/src/components/` (6 komponen), `App.jsx`, `api.js` |
| Verina | QA & Dokumentasi | `README.md` (9×), `auth-test-result.md`, `ui-test-results.md` + 12 screenshot UI |
| Cintya | Setup Guide & Info | `docs/setup-guide.md`, `README.md`, `.env.example` |

---

## C. Penilaian Tugas Terstruktur (5% Semester)

### Rubrik per Minggu

#### Minggu 1 — Cloud Fundamentals & Setup
| Kriteria | Bobot | Skor | Keterangan |
|----------|:---:|:---:|-----------|
| README.md lengkap (team, arsitektur, tech stack, getting started) | 30% | 28 | README 1034 baris, sangat komprehensif |
| Endpoint `/team` dengan data anggota aktual | 30% | 27 | ✅ Ada, data lengkap. Catatan: NIM Verina salah (`1023109` harusnya `10231090`) |
| Roadmap & rencana proyek terdokumentasi | 20% | 18 | ✅ Ada di README |
| Struktur repo rapi & .gitignore benar | 20% | 17 | ✅ .gitignore ada, .env tidak tercommit |
| **Subtotal Minggu 1** | | **90/100** | |

#### Minggu 2 — Backend REST API (FastAPI + PostgreSQL)
| Kriteria | Bobot | Skor | Keterangan |
|----------|:---:|:---:|-----------|
| ≥4 endpoint CRUD fungsional | 30% | 30 | ✅ `GET/POST/PUT/DELETE /items`, `/items/stats`, `/health` |
| Koneksi PostgreSQL via SQLAlchemy | 25% | 25 | ✅ `database.py` benar, model `Item` terdefinisi |
| Pydantic schema & validasi | 25% | 23 | ✅ Field validator, min/max, gt=0 — baik |
| HTTP status code tepat | 20% | 18 | ✅ 201 create, 204 delete, 404 not found |
| **Subtotal Minggu 2** | | **96/100** | |

#### Minggu 3 — Frontend React
| Kriteria | Bobot | Skor | Keterangan |
|----------|:---:|:---:|-----------|
| ≥3 komponen React terpisah & terstruktur | 30% | 30 | ✅ 5 komponen: Header, ItemCard, ItemForm, ItemList, SearchBar |
| CRUD UI fungsional (tampil, tambah, edit, hapus) | 30% | 28 | ✅ Lengkap + empty state + loading state |
| Validasi form (required, positive number, dll) | 20% | 18 | ✅ Ada validasi, tapi minor: LoginPage.jsx belum divalidasi sepenuhnya |
| Integrasi API dengan error handling (401, dll) | 20% | 18 | ✅ Token management, intercept 401 |
| **Subtotal Minggu 3** | | **94/100** | |

#### Minggu 4 — Full-Stack Integration (CORS, .env, JWT)
| Kriteria | Bobot | Skor | Keterangan |
|----------|:---:|:---:|-----------|
| CORS whitelist (bukan `*`) via env | 25% | 23 | ✅ Whitelist dari `.env`, tapi `allow_methods=["*"]` dan `allow_headers=["*"]` |
| Semua secret di `.env`, tidak hardcode | 25% | 20 | ⚠️ `.env.example` mencantumkan SECRET_KEY nyata & password DB (`Nazwa2`) — risiko kebocoran |
| JWT auth end-to-end (register → login → protected) | 35% | 30 | ✅ Lengkap: register, login, `/auth/me`, proteksi semua endpoint |
| Protected routes di frontend | 15% | 14 | ✅ Ada, token disimpan dan digunakan |
| **Subtotal Minggu 4** | | **87/100** | Dikurangi karena isu keamanan di `.env.example` dan DEBUG print yang bocorkan token |

---

### Rekapitulasi Nilai Tugas Kelompok

| Minggu | Subtotal | Bobot Sama | Kontribusi |
|--------|:---:|:---:|:---:|
| Minggu 1 | 90 | 25% | 22.5 |
| Minggu 2 | 96 | 25% | 24.0 |
| Minggu 3 | 94 | 25% | 23.5 |
| Minggu 4 | 87 | 25% | 21.75 |
| **TOTAL TUGAS KELOMPOK** | | | **91.75 / 100** |

**Nilai Huruf: A (Luar Biasa)** — Skala 86–100

---

## D. Penilaian Sikap & Profesionalisme Individual (5% Semester)
*Instrument: Partisipasi dan kontribusi mingguan via Git log — sesuai RPS*

### Rubrik Penilaian Individu

| Kriteria | Bobot |
|----------|:---:|
| Aktif commit setiap minggu (konsistensi) | 30% |
| Kualitas & substansi kontribusi (bukan hanya README/upload) | 40% |
| Kesesuaian kerja dengan peran yang diemban | 20% |
| Commit message informatif | 10% |

---

### 1. Ahmad Daffa Alfattah (NIM: 10231008) — Lead Backend

| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu: 6/3/4/4) | 30/30 |
| Substansi: `main.py`, `auth.py`, `crud.py`, `models.py`, `schemas.py` — core backend sepenuhnya | 38/40 |
| Sesuai peran Backend: 100% file backend + auth | 20/20 |
| Commit message: deskriptif (`feat: add JWT authentication`, dll) | 8/10 |
| **Total** | **96/100** |

**Catatan:** Kualitas kode backend sangat baik. Satu catatan: terdapat banyak `print(f"[DEBUG]...")` di `auth.py` yang mencetak nilai token ke log — risiko keamanan, seharusnya dihapus setelah development.

**Nilai: A (Luar Biasa)**

---

### 2. Nazwa Amelia Zahra (NIM: 10231068) — Lead Frontend

| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu: 8/3/3/2) | 28/30 |
| Substansi: 5 komponen React, `App.jsx`, `api.js` — frontend sepenuhnya | 37/40 |
| Sesuai peran Frontend: 100% file frontend | 19/20 |
| Commit message: deskriptif (`feat: add React CRUD frontend...`, dll) | 8/10 |
| **Total** | **92/100** |

**Catatan:** Kontribusi frontend sangat baik dan konsisten. Sedikit penurunan di Minggu 4 (2 commit), namun substansi commit tetap berkualitas.

**Nilai: A (Luar Biasa)**

---

### 3. Verina Rahma Dinah (NIM: 10231090) — Lead QA & Docs

| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu: 5/5/2/3) | 28/30 |
| Substansi: README komprehensif (1034 baris), auth-test-result.md (161 baris), 32 screenshot pengujian | 36/40 |
| Sesuai peran QA & Docs: semua kontribusi di dokumentasi dan pengujian | 18/20 |
| Commit message: deskriptif (`docs: add API endpoints documentation...`, dll) | 9/10 |
| **Total** | **91/100** |

**Catatan:** Dokumentasi terbaik di kelompok. README sangat lengkap, test documentation dengan screenshots sangat rapi. Namun tidak ada kontribusi kode aplikasi — sesuai peran QA & Docs tapi perlu juga memahami kode yang didokumentasikan.

**Nilai: A (Luar Biasa)**

---

### 4. Cintya Widhi Astuti (NIM: 10231026) — Lead DevOps

| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu: 2/1/1/2) | 20/30 |
| Substansi: hanya `setup-guide.md`, README upload, `.env.example` — tidak ada kontribusi DevOps aktual | 18/40 |
| Sesuai peran DevOps: 0% implementasi Docker/Infrastructure (belum waktunya Minggu 5, tapi setup environment, docs DevOps bisa dilakukan) | 10/20 |
| Commit message: kurang deskriptif (`uplode setup-guide` — typo, duplikat commit) | 5/10 |
| **Total** | **53/100** |

**Catatan Penting:**
- Duplikat commit: "uplode setup-guide" muncul 2x pada tanggal yang sama (17 Mar) — perlu diperbaiki ke depannya
- Typo konsisten pada commit message ("uplode" bukan "upload")
- Untuk Minggu 1–4, kontribusi DevOps memang masih terbatas karena Docker baru dimulai Minggu 5, namun kontribusi overall sangat jauh di bawah anggota lain (6 vs 15–17 commit)
- Perlu peningkatan signifikan di Minggu 5–7 (Docker) sesuai perannya
- Inkonsistensi nama peran: `member-[cintya].md` menyebut "Dev Ops" tapi `/team` endpoint menyebut "Lead QA & Docs"

**Nilai: C (Cukup)** — Perlu peningkatan kontribusi nyata sesuai peran

---

## E. Rekapitulasi Nilai Akhir

### Nilai Tugas Kelompok
| Komponen RPS | Bobot Semester | Skor | Nilai |
|-------------|:---:|:---:|:---:|
| Tugas Terstruktur Minggu 1-4 | 5% | 91.75 | **A** |

### Nilai Individu — Sikap & Profesionalisme
| Nama | NIM | Skor | Nilai Huruf |
|------|-----|:---:|:---:|
| Ahmad Daffa Alfattah | 10231008 | 96 | **A** |
| Nazwa Amelia Zahra | 10231068 | 92 | **A** |
| Verina Rahma Dinah | 10231090 | 91 | **A** |
| Cintya Widhi Astuti | 10231026 | 53 | **C** |

---

## F. Catatan & Rekomendasi untuk Kelompok

### Yang Sudah Baik ✅
1. Aplikasi full-stack lengkap: FastAPI + React + PostgreSQL + JWT Auth
2. Dokumentasi sangat komprehensif (README 1034 baris, 32+ screenshot pengujian)
3. Semua 4 anggota aktif commit setiap minggu
4. Validasi input kuat (Pydantic field_validator, password strength)
5. CORS sudah menggunakan whitelist dari env (bukan `*`)
6. `.env` tidak tercommit ke repo

### Yang Perlu Diperbaiki ⚠️
1. **[Keamanan - SEGERA]** `auth.py`: Hapus semua `print(f"[DEBUG]...")` yang mencetak nilai token — berbahaya jika masuk production logs
2. **[Keamanan]** `.env.example`: Jangan masukkan password/secret asli (ganti `Nazwa2` dengan `your_password_here`)
3. **[Bug Minor]** NIM Verina di endpoint `/team` salah: `"1023109"` harusnya `"10231090"`
4. **[Inkonsistensi]** Peran Cintya berbeda antara `member-[cintya].md` ("Dev Ops") dan `/team` endpoint ("Lead QA & Docs") — perlu diseragamkan
5. **[Cintya]** Tingkatkan kontribusi signifikan di Minggu 5–7 (Dockerfile, Docker Compose) sesuai peran DevOps

---

*Dokumen ini dibuat berdasarkan analisis langsung dari git log dan kode sumber repository. Semua data commit terverifikasi.*
