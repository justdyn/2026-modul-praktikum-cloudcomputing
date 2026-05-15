# Laporan Penilaian Kelompok miracle – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | miracle |
| Repo | cc-kelompok-a-miracle |
| Project | **Donor Manajemen** — Sistem manajemen pendonor & riwayat donor darah (dilihat dari tabel `test_pendonor.py`, `test_riwayat_donor.py`) |

**Anggota (5 anggota, role split granular):**

| Nama | NIM | Role |
|---|---|---|
| Avhilla Catton Andalucia | 10231021 | Lead Container |
| Betran | 10231023 | Lead QA & Docs |
| Chelsy Olivia | 10231025 | Lead CI/CD & Deploy |
| Debora Intania Subekti | 10231029 | Lead Backend |
| Yosan Pratiwi | 10231091 | Lead Frontend |

---

### A. Penilaian Kelompok – Foundation Project

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **86** | README dengan team table 5 anggota, role split granular (Container + CI/CD terpisah). `CHANGELOG.md` ada. Dokumentasi screenshot tersedia (image-1.png … image-5.jpeg). |
| **M2 – Backend CRUD domain-specific** | 25% | **86** | 27 routes (`main.py`), layered structure (models/schemas/crud/auth/database), `ruff.toml`, `pytest.ini`, `tests/`, helper `scripts/`, `test_db_connection.py` + `test_pagination.py` di root backend (utility scripts). |
| **M3 – Frontend domain-specific** | 25% | **84** | Standar React+Vite. |
| **M4 – Auth + CORS + .env** | 25% | **86** | JWT, CORS dari `ALLOWED_ORIGINS` env, `python-dotenv`. Minus: fallback `SECRET_KEY = "fallback-secret-key-for-development"` (`auth.py:18`). |

**Nilai Kelompok: (86 + 86 + 84 + 86) / 4 = 85.50 → 86**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual

> **Catatan alias:** Avhilla = `Avhilla Catton Andalucia` + `Avhilla`. Betran = `BETRAN` + `Betran` + `piz4rroo`. Chelsy = `Chelsy Olivia` + `chelolv15`. Debora = `Debora Intania Subekti` + `intniaaa20`.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Debora Intania Subekti | intniaaa20 | 15 | 4 | 1 | 6 | **26** |
| Yosan Pratiwi | Yosan Pratiwi | 4 | 3 | 3 | 4 | **14** |
| Avhilla Catton Andalucia | Avhilla Catton Andalucia | 5 | 1 | 2 | 5 | **13** |
| Chelsy Olivia | Chelsy Olivia | 6 | 1 | 1 | 2 | **10** |
| Betran | BETRAN / Betran / piz4rroo | 7 | 1 | 1 | 1 | **10** |

---

### C. Penilaian Individual

#### 1. Debora Intania Subekti (Lead Backend)
- **Konsistensi (30%):** 4/4 → 92 · **Substansi (40%):** 26 commits — tertinggi tim → 92 · **Peran (20%):** Backend → 90 · **Pesan (10%):** → 80

**Nilai: 27.6 + 36.8 + 18.0 + 8.0 = 90.4 → 90** · **Grade: A**

---

#### 2. Yosan Pratiwi (Lead Frontend)
- **Konsistensi (30%):** 4/4 → 92 · **Substansi (40%):** 14 commits → 84 · **Peran (20%):** Frontend → 88 · **Pesan (10%):** → 78

**Nilai: 27.6 + 33.6 + 17.6 + 7.8 = 86.6 → 87** · **Grade: A**

---

#### 3. Avhilla Catton Andalucia (Lead Container)
- **Konsistensi (30%):** 4/4 → 90 · **Substansi (40%):** 13 commits → 82 · **Peran (20%):** Container belum F1 prime → 76 · **Pesan (10%):** → 78

**Nilai: 27.0 + 32.8 + 15.2 + 7.8 = 82.8 → 83** · **Grade: AB**

---

#### 4. Chelsy Olivia (Lead CI/CD & Deploy)
- **Konsistensi (30%):** 4/4 → 88 · **Substansi (40%):** 10 commits → 78 · **Peran (20%):** CI/CD belum F1 prime → 72 · **Pesan (10%):** → 78

**Nilai: 26.4 + 31.2 + 14.4 + 7.8 = 79.8 → 80** · **Grade: AB**

---

#### 5. Betran (Lead QA & Docs)
- **Konsistensi (30%):** 4/4 → 88 · **Substansi (40%):** 10 commits → 78 · **Peran (20%):** QA & Docs → 84 · **Pesan (10%):** → 75

**Nilai: 26.4 + 31.2 + 16.8 + 7.5 = 81.9 → 82** · **Grade: AB**

---

### D. Ringkasan untuk Gradebook

**C02 (5%):** semua anggota **86**

**C03 (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231021 | Avhilla Catton Andalucia | **83** |
| 10231023 | Betran | **82** |
| 10231025 | Chelsy Olivia | **80** |
| 10231029 | Debora Intania Subekti | **90** |
| 10231091 | Yosan Pratiwi | **87** |
