# Laporan Penilaian Kelompok awit – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | awit |
| Repo | cc-kelompok-a-awit |
| Kelas | A |
| Project | **PalmTrack Cloud (PalmChain)** — Sistem informasi cloud-native untuk pencatatan & monitoring pengangkutan TBS kelapa sawit dari kebun ke pabrik |

**Anggota (dari `Readme.md` + `/team` endpoint `backend/main.py:546`):**

| Nama | NIM | Role |
|---|---|---|
| Adam Ibnu Ramadhan | 10231003 | Lead Backend |
| Adhyasta Firdaus | 10231005 | Lead CI/CD & Deployment |
| Adonia Azarya Tamalonggehe | 10231007 | Lead QA & Documentation |
| Alfian Fadillah Putra | 10231009 | Lead Frontend |
| Varrel Kaleb Ropard Pasaribu | 10231089 | Lead DevOps & Container |

> 5 anggota dengan **split role** Container + CI/CD + DevOps terpisah (paling granular di kelas A).

---

### A. Penilaian Kelompok – Foundation Project

> 4 kriteria @ 25%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **90** | `Readme.md` sangat profesional: project brief jelas (PalmTrack TBS hauling tracker), fitur utama (Manajemen Akses, Vendor, Blok Panen, Actual Hauling, Dashboard), tech stack table dengan versi, **Mermaid architecture diagram**, struktur proyek tree. `/team` endpoint ada. Member docs lengkap di `docs/member-[Nama].md` per anggota. |
| **M2 – Backend CRUD domain-specific** | 25% | **86** | Backend FastAPI 28 routes sesuai domain TBS (vendors, blok panen, hauling, dashboard stats). Layered: `models.py`, `schemas.py`, `crud.py`, `database.py`, `auth.py`, folder `migrations/`, `palmchain_schema.sql` (raw SQL backup). `pytest.ini` + `tests/`. `ruff.toml` untuk linting. |
| **M3 – Frontend domain-specific** | 25% | **86** | React 19 + Vite 7 + **Recharts** untuk visualisasi dashboard (sesuai domain). `nginx.conf`, ESLint config, struktur `src/`. |
| **M4 – Auth + CORS + .env** | 25% | **86** | JWT via `python-jose`. CORS `ALLOWED_ORIGINS` dari env (`main.py:33`). `python-dotenv` aktif. Minus: fallback `SECRET_KEY = "fallback-secret-key-for-development"` di `auth.py:19` (perlu di-flag untuk M15 security audit). |

**Nilai Kelompok: (90 + 86 + 86 + 86) / 4 = 87.00**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W1–W4)

> **Catatan alias:** Adam = `adamimir` + `Adam IR`. Adhyasta = `Adhyasta Firdaus` + `adhyasta firdaus`. Alfian pakai 2 email (kampus + GitHub noreply). Varrel = `VarrelKaleb89` + `VarrelKaleb` + `unknown` (email `varrelpassaribu@gmail.com`, bukan email ITK).

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Alfian Fadillah Putra | Alfian Fadillah Putra | 10 | 3 | 3 | 1 | **17** |
| Adam Ibnu Ramadhan | adamimir | 3 | 4 | 0 | 5 | **12** |
| Adonia Azarya Tamalonggehe | Adonia Azarya Tamalonggehe | 1 | 2 | 2 | 1 | **6** |
| Adhyasta Firdaus | Adhyasta Firdaus | 1 | 1 | 1 | 2 | **5** |
| Varrel Kaleb Ropard Pasaribu | VarrelKaleb / unknown | 0 | 2 | 1 | 2 | **5** |

---

### C. Penilaian Individual

#### 1. Alfian Fadillah Putra (Lead Frontend)
- **Konsistensi (30%):** 4/4 minggu aktif → 92
- **Substansi (40%):** 17 commits, tertinggi kelompok. Frontend implementation + initial setup → 90
- **Kesesuaian Peran (20%):** Frontend dominant → 88
- **Kualitas Pesan (10%):** Mix → 80

**Nilai: (0.30×92 + 0.40×90 + 0.20×88 + 0.10×80) = 27.6 + 36.0 + 17.6 + 8.0 = 89.2 → 89**
**Grade: A**

---

#### 2. Adam Ibnu Ramadhan (Lead Backend)
- **Konsistensi (30%):** 3/4 minggu aktif (W3 kosong) → 80
- **Substansi (40%):** 12 commits backend → 84
- **Kesesuaian Peran (20%):** Backend → 86
- **Kualitas Pesan (10%):** Cukup deskriptif → 78

**Nilai: (0.30×80 + 0.40×84 + 0.20×86 + 0.10×78) = 24.0 + 33.6 + 17.2 + 7.8 = 82.6 → 83**
**Grade: AB**

---

#### 3. Adonia Azarya Tamalonggehe (Lead QA & Documentation)
- **Konsistensi (30%):** 4/4 minggu aktif → 88
- **Substansi (40%):** 6 commits docs/QA → 72
- **Kesesuaian Peran (20%):** Docs (member-docs, api-documentation) → 86
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×88 + 0.40×72 + 0.20×86 + 0.10×75) = 26.4 + 28.8 + 17.2 + 7.5 = 79.9 → 80**
**Grade: AB**

---

#### 4. Adhyasta Firdaus (Lead CI/CD & Deployment)
- **Konsistensi (30%):** 4/4 minggu aktif → 86
- **Substansi (40%):** 5 commits — role CI/CD belum prime time di F1 → 68
- **Kesesuaian Peran (20%):** Sedikit cross-role karena CI/CD belum dimulai → 72
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×86 + 0.40×68 + 0.20×72 + 0.10×75) = 25.8 + 27.2 + 14.4 + 7.5 = 74.9 → 75**
**Grade: B**

---

#### 5. Varrel Kaleb Ropard Pasaribu (Lead DevOps & Container)
- **Konsistensi (30%):** 3/4 minggu aktif (W1 kosong) → 75
- **Substansi (40%):** 5 commits, container belum prime time di F1 → 65
- **Kesesuaian Peran (20%):** → 70
- **Kualitas Pesan (10%):** Email `varrelpassaribu@gmail.com` bukan ITK, kadang muncul sebagai `unknown` → 65

**Nilai: (0.30×75 + 0.40×65 + 0.20×70 + 0.10×65) = 22.5 + 26.0 + 14.0 + 6.5 = 69.0 → 69**
**Grade: B**

---

### D. Ringkasan untuk Gradebook

**C02 — Tugas terstruktur kelompok (5%):** semua anggota **87**

**C03 — Partisipasi & kontribusi mingguan via Git log (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231003 | Adam Ibnu Ramadhan | **83** |
| 10231005 | Adhyasta Firdaus | **75** |
| 10231007 | Adonia Azarya Tamalonggehe | **80** |
| 10231009 | Alfian Fadillah Putra | **89** |
| 10231089 | Varrel Kaleb Ropard Pasaribu | **69** |
