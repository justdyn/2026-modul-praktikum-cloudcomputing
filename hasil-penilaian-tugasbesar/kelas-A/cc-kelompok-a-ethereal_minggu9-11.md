# Laporan Penilaian Kelompok ethereal – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ethereal |
| Repo | cc-kelompok-a-ethereal |
| Fase | M9 (Git workflow + PR) → M10 (GitHub Actions) → M11 (Tests + coverage + badge) |

---

### A. Penilaian Kelompok – CI/CD

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **78** | `.github/CODEOWNERS` + `.github/pull_request_template.md` + `docs/git-workflow.md` (panduan tim). **Minus:** sangat sedikit PR ter-merge yang terlihat di fase ini — mayoritas commit direct ke main meski infra PR sudah siap. |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **95** | `.github/workflows/ci.yml` punya **5 jobs**: lint (ruff, `permissions: pull-requests:write`), test-backend (`needs: [lint]`, gated coverage), test-frontend (Vitest build), build-docker (gated `needs: [test-backend, test-frontend]`), **notify-failure** (PR comment otomatis via `thollander/actions-comment-pull-request@v2` jika ada job gagal). Concurrency cancel, timeout per job, env DATABASE_URL untuk testing. **Paling advanced di kelas A** untuk M10. |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **88** | Backend tests: `test_auth.py`, `test_health.py`, `test_tasks.py` + `conftest.py`. Frontend Vitest setup. **CI badge muncul di `README.md` baris 2** (`![CI Pipeline](...)`). Dokumentasi: `docs/testing-guide.md` (+PDF), `docs/git-workflow.md`. Coverage report aktif (`--cov=. --cov-report=term-missing`). |

**Nilai Kelompok: (78 + 95 + 88) / 3 = 87.00**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W9–W11)

> W9 = 20–26 Apr, W10 = 27 Apr – 3 Mei, W11 = 4–10 Mei. **W11 burst** seluruh tim (sprint final pre-fase 5).

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Tiya Mitra Ayu | Tiyamitraayu / Tiyamitrayu | 0 | 0 | 14 | **14** |
| Amazia Devid Saputra | Devid / Devid1013 | 2 | 0 | 11 | **13** |
| Alsha Dwi Cahya | dwialsha | 0 | 0 | 11 | **11** |
| Andini Permata Sari | gitandys | 3 | 0 | 8 | **11** |
| Ansellma Tita Pakartiwuri | secretceremony | 0 | 1 | 3 | **4** |

---

### C. Penilaian Individual

#### 1. Andini Permata Sari (Lead QA & Docs)
- **Konsistensi (30%):** 2/3 minggu aktif → 80
- **Substansi (40%):** 11 commits — paling konsisten di kelompok. Testing-guide, git-workflow docs, dukung CI → 80
- **Kesesuaian Peran (20%):** 100% docs/test docs → 86
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×80 + 0.40×80 + 0.20×86 + 0.10×78) = 24.0 + 32.0 + 17.2 + 7.8 = 81.0 → 81**
**Grade: AB**

---

#### 2. Amazia Devid Saputra (Lead Frontend)
- **Konsistensi (30%):** 2/3 minggu aktif → 75
- **Substansi (40%):** 13 commits → 84
- **Kesesuaian Peran (20%):** Frontend + tests → 86
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×75 + 0.40×84 + 0.20×86 + 0.10×78) = 22.5 + 33.6 + 17.2 + 7.8 = 81.1 → 81**
**Grade: AB**

---

#### 3. Tiya Mitra Ayu (Lead Backend)
- **Konsistensi (30%):** 1/3 minggu aktif (W11 only) → 65
- **Substansi (40%):** 14 commits — tertinggi tim, burst W11 → 84
- **Kesesuaian Peran (20%):** Backend tests + features → 84
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×65 + 0.40×84 + 0.20×84 + 0.10×78) = 19.5 + 33.6 + 16.8 + 7.8 = 77.7 → 78**
**Grade: AB**

---

#### 4. Ansellma Tita Pakartiwuri Putri (Lead Deploy & CI/CD)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 4 commits — **role CI/CD prime time** tapi volume rendah. Quality of CI workflow sangat tinggi (5 jobs + notify-failure) — ada kemungkinan dia author utama `ci.yml` → 72
- **Kesesuaian Peran (20%):** CI/CD pipeline-nya terbaik di kelas → 88
- **Kualitas Pesan (10%):** → 80

**Nilai: (0.30×72 + 0.40×72 + 0.20×88 + 0.10×80) = 21.6 + 28.8 + 17.6 + 8.0 = 76.0 → 76**
**Grade: AB**

> Volume rendah tapi *impact per commit* tinggi (ci.yml dengan 5 jobs adalah masterpiece).

---

#### 5. Alsha Dwi Cahya (Lead Container)
- **Konsistensi (30%):** 1/3 minggu aktif → 60
- **Substansi (40%):** 11 commits W11 → 80
- **Kesesuaian Peran (20%):** Container/build → 84
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×60 + 0.40×80 + 0.20×84 + 0.10×75) = 18.0 + 32.0 + 16.8 + 7.5 = 74.3 → 74**
**Grade: B**

---

### D. Ringkasan untuk Gradebook

**C12 — Tugas CI/CD pipeline + badge hijau (3%):** semua anggota **87**

**C13 — Kontribusi via Git commit log + PR history (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231011 | Alsha Dwi Cahya | **74** |
| 10231013 | Amazia Devid Saputra | **81** |
| 10231015 | Andini Permata Sari | **81** |
| 10231017 | Ansellma Tita Pakartiwuri Putri | **76** |
| 10231088 | Tiya Mitra Ayu | **78** |

---

### E. Tren Lintas Fase (ethereal)

| Anggota | F1 | F2 | F4 | Tren |
|---|:---:|:---:|:---:|---|
| Alsha (Container) | 83 | 78 | 74 | Menurun bertahap |
| Devid (Frontend) | 85 | 76 | 81 | Recover di F4 |
| Andini (QA & Docs) | 78 | 75 | 81 | Naik di F4 |
| Ansel (Deploy & CI/CD) | 77 | 71 | 76 | Stabil ~76 |
| Tiya (Backend) | 82 | 55 | 78 | Recover tajam dari F2 dip |

**Nilai kelompok:** F1=83, F2=87, F4=87 → stabil di range A-AB.
