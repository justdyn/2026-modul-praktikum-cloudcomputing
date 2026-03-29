# Laporan Penilaian Tugas Terstruktur — Minggu 1-4
**Kelompok:** cc-kelompok-bismillah_a
**Tanggal Penilaian:** 29 Maret 2026

---

## A. Identitas Kelompok

| Nama | NIM | Peran |
|------|-----|-------|
| Aditya Laksamana P Butar Butar | 10231006 | Lead Backend |
| Firni Fauziah Ramadhini | 10231038 | Lead Frontend |
| Muhammad Novri Aziztra | 10231066 | Lead DevOps |
| Salsabila Putri Zahrani | 10231086 | Lead QA & Docs |

---

## B. Rekap Kontribusi Git (TERVERIFIKASI)

| Anggota | Minggu 1 (W9) | Minggu 2 (W10) | Minggu 3 (W11) | Minggu 4 (W12) | Total Scope |
|---------|:---:|:---:|:---:|:---:|:---:|
| Aditya Laksamana | 11 | 2 | 3 | 4 | **20** |
| Firni Fauziah | 4 | 3 | 2 | 3 | **12** |
| Muhammad Novri | 5 | 1 | 2 | **0** ⚠️ | 8 |
| Salsabila Putri | 3 | 3 | 1 | 1 | **8** |

> ⚠️ Novri tidak memiliki commit di Minggu 4 (W12).
> Catatan: Aditya menggunakan 2 akun git (10231006@student + gmail) — 20 commit adalah gabungan dari kedua akun.

### Area Kontribusi per Anggota
| Anggota | File Kunci yang Disentuh |
|---------|------------------------|
| Aditya | `backend/main.py`, `auth.py`, `crud.py`, `schemas.py`, `models.py` — core backend |
| Firni | `frontend/src/component/` — komponen React, `App.jsx`, `api.js` |
| Novri | `backend/`, infrastructure docs |
| Salsabila | `README.md`, `docs/` — dokumentasi & testing |

---

## C. Penilaian Tugas Terstruktur Kelompok

| Minggu | Kriteria Utama | Skor | Catatan |
|--------|---------------|:---:|---------|
| **M1** | README 287 baris (cukup), /team ✅ NIMs benar, struktur bersih | **85** | README lebih singkat dibanding rata-rata |
| **M2** | `main.py` 204 baris, CRUD lengkap, auth.py ✅, PostgreSQL ✅ | **93** | Backend solid |
| **M3** | 6 komponen di `frontend/src/component/` ✅, CRUD UI lengkap | **90** | Folder `component/` (bukan `components/`) — minor naming inconsistency |
| **M4** | CORS whitelist ✅, .env tidak tercommit ✅, JWT ✅, endpoint terlindungi ✅ | **90** | Implementasi Minggu 4 lengkap |

**Total Tugas Kelompok: (85+93+90+90)/4 = 89.5 / 100 → A (Luar Biasa)**

---

## D. Penilaian Individu — Sikap & Profesionalisme

### 1. Aditya Laksamana P Butar Butar (10231006) — Lead Backend
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 20 total) | 30/30 |
| Substansi: seluruh file backend (main, auth, crud, schemas, models) | 37/40 |
| Sesuai peran Backend ✅ | 20/20 |
| Commit message informatif | 8/10 |
| **Total** | **95/100 → A** |

### 2. Firni Fauziah Ramadhini (10231038) — Lead Frontend
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 12 total) | 28/30 |
| Substansi: komponen React, App.jsx, api.js ✅ | 35/40 |
| Sesuai peran Frontend ✅ | 18/20 |
| Commit message cukup deskriptif | 7/10 |
| **Total** | **88/100 → AB** |

### 3. Muhammad Novri Aziztra (10231066) — Lead DevOps
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (⚠️ W12 tidak ada commit — 3 dari 4 minggu aktif) | 20/30 |
| Substansi: kontribusi backend/docs — DevOps (Docker) belum waktunya | 26/40 |
| Sesuai peran DevOps: belum ada artefak Docker (wajar Wk5) | 13/20 |
| Commit message cukup | 7/10 |
| **Total** | **66/100 → B** |
> Perlu memastikan konsistensi kontribusi di setiap pekan. Minggu 4 tidak ada commit sama sekali.

### 4. Salsabila Putri Zahrani (10231086) — Lead QA & Docs
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 8 dalam scope) | 27/30 |
| Substansi: README, docs/ — dokumentasi cukup | 28/40 |
| Sesuai peran QA & Docs ✅ | 17/20 |
| Commit message deskriptif | 7/10 |
| **Total** | **79/100 → B** |

---

## E. Catatan & Rekomendasi

**Yang Sudah Baik ✅**
- Aplikasi full-stack lengkap (FastAPI + React + JWT + PostgreSQL)
- /team endpoint benar dengan NIM yang tepat
- Semua anggota aktif, tidak ada yang nol kontribusi
- Struktur repo bersih, tidak ada .env tercommit

**Yang Perlu Diperbaiki ⚠️**
1. Novri: tidak ada commit di Minggu 4 — perlu konsistensi
2. Folder frontend `component/` sebaiknya diseragamkan menjadi `components/` (konvensi standar React)
3. README bisa lebih detail (287 baris tergolong minimal untuk Week 1-4)
4. Aditya: gunakan 1 akun git yang konsisten untuk tracking yang lebih rapi
