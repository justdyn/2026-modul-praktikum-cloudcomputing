# Laporan Penilaian Kelompok awit – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | awit |
| Repo | cc-kelompok-a-awit |
| Fase | M9 (Git workflow + PR) → M10 (GitHub Actions) → M11 (Tests + coverage + badge) |

---

### A. Penilaian Kelompok – CI/CD

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **96** | **10+ PR ter-merge** dalam fase ini (PR #12 s/d #22). Conventional commits konsisten (`feat:`, `fix:`, `ci:`, `test:`, `chore:`). `CODEOWNERS` di `.github/CODEOWNERS`. **`pull_request_template.md` di `.github/`** (di atas kelompok lain). |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **96** | `.github/workflows/ci.yml` punya **4 jobs**: lint (ruff), test-backend (pytest + coverage `--cov-fail-under=50`), test-frontend (Vitest + npm build), build-docker (gated `needs: [test-backend, test-frontend]`). Concurrency cancel-in-progress, pip+npm cache, timeout 10 menit per job. Best-in-class. |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **92** | Backend tests: `test_auth.py`, `test_health.py`, `test_items.py` + `conftest.py`. Frontend Vitest setup. CI badge ditambahkan via PR #19 (`fix: resolve test errors, add CI badge, and optimize pipeline`). Edge case tests + endpoint stats di PR #21. |

**Nilai Kelompok: (96 + 96 + 92) / 3 = 94.67 → 95**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W9–W11)

> W9 = 20–26 Apr, W10 = 27 Apr – 3 Mei, W11 = 4–10 Mei.

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Adhyasta Firdaus | Adhyasta Firdaus / adhyasta firdaus | 3 | 3 | 1 | **7** |
| Varrel Kaleb Ropard Pasaribu | VarrelKaleb89 | 0 | 0 | 5 | **5** |
| Alfian Fadillah Putra | Alfian Fadillah Putra | 0 | 0 | 4 | **4** |
| Adam Ibnu Ramadhan | Adam IR | 0 | 0 | 2 | **2** |
| Adonia Azarya Tamalonggehe | Adonia Azarya Tamalonggehe | 1 | 0 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Adhyasta Firdaus (Lead CI/CD & Deployment)
- **Konsistensi (30%):** 3/3 minggu aktif → 95
- **Substansi (40%):** 7 commits — **role CI/CD prime time**. Setup GitHub Actions workflow, ruff lint integration, CI badge → 95
- **Kesesuaian Peran (20%):** 100% match role → 98
- **Kualitas Pesan (10%):** Conventional commits eksplisit (`ci: add GitHub Actions workflow...`, `ci: add ruff linting to pipeline`) → 88

**Nilai: (0.30×95 + 0.40×95 + 0.20×98 + 0.10×88) = 28.5 + 38.0 + 19.6 + 8.8 = 94.9 → 95**
**Grade: A**

> 🚀 Naik tajam dari F1 (75) & F2 (61) → F4 (95). Role-fit pemain inti F4.

---

#### 2. Varrel Kaleb Ropard Pasaribu (Lead DevOps & Container)
- **Konsistensi (30%):** 1/3 minggu aktif (W11 only) → 60
- **Substansi (40%):** 5 commits → 75
- **Kesesuaian Peran (20%):** Container/CI build → 80
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×60 + 0.40×75 + 0.20×80 + 0.10×78) = 18.0 + 30.0 + 16.0 + 7.8 = 71.8 → 72**
**Grade: B**

---

#### 3. Alfian Fadillah Putra (Lead Frontend)
- **Konsistensi (30%):** 1/3 minggu aktif → 60
- **Substansi (40%):** 4 commits — dark mode + Vitest setup → 75
- **Kesesuaian Peran (20%):** Frontend tests + features → 84
- **Kualitas Pesan (10%):** Conventional commits (`feat(frontend):...`) → 82

**Nilai: (0.30×60 + 0.40×75 + 0.20×84 + 0.10×82) = 18.0 + 30.0 + 16.8 + 8.2 = 73.0 → 73**
**Grade: B**

---

#### 4. Adam Ibnu Ramadhan (Lead Backend)
- **Konsistensi (30%):** 1/3 minggu aktif → 55
- **Substansi (40%):** 2 commits backend test → 60
- **Kesesuaian Peran (20%):** Backend → 78
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×55 + 0.40×60 + 0.20×78 + 0.10×78) = 16.5 + 24.0 + 15.6 + 7.8 = 63.9 → 64**
**Grade: BC**

---

#### 5. Adonia Azarya Tamalonggehe (Lead QA & Documentation)
- **Konsistensi (30%):** 1/3 minggu aktif → 50
- **Substansi (40%):** 1 commit → 50
- **Kesesuaian Peran (20%):** Docs → 65
- **Kualitas Pesan (10%):** → 70

**Nilai: (0.30×50 + 0.40×50 + 0.20×65 + 0.10×70) = 15.0 + 20.0 + 13.0 + 7.0 = 55.0 → 55**
**Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C12 — Tugas CI/CD pipeline + badge hijau (3%):** semua anggota **95**

**C13 — Kontribusi via Git commit log + PR history (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231003 | Adam Ibnu Ramadhan | **64** |
| 10231005 | Adhyasta Firdaus | **95** |
| 10231007 | Adonia Azarya Tamalonggehe | **55** |
| 10231009 | Alfian Fadillah Putra | **73** |
| 10231089 | Varrel Kaleb Ropard Pasaribu | **72** |

---

### E. Tren Lintas Fase (awit)

| Anggota | F1 (M1-4) | F2 (M5-7) | F4 (M9-11) | Tren |
|---|:---:|:---:|:---:|---|
| Adam Ibnu Ramadhan (Backend) | 83 | 73 | 64 | Menurun bertahap |
| Adhyasta Firdaus (CI/CD) | 75 | 61 | **95** | **Naik tajam di F4** (role prime time) |
| Adonia Azarya (QA & Docs) | 80 | 54 | 55 | Drop setelah F1 |
| Alfian Fadillah Putra (Frontend) | 89 | 69 | 73 | Drop setelah F1 |
| Varrel Kaleb (DevOps & Container) | 69 | 82 | 72 | Naik di F2 (role prime time), turun lagi |

**Nilai kelompok:** F1=87, F2=91, F4=95 → konsisten naik. Role-split granular terbukti efektif di fase teknis.
