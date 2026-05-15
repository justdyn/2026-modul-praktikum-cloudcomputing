# Laporan Penilaian Kelompok bismillah_a – Kelas B
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### A. Penilaian Kelompok – CI/CD

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **95** | **14+ PR ter-merge dalam F4** (#10 CI pipeline, #11 frontend Vitest tests, #12 more backend tests, #13 CI optimization, #14 testing-guide, #15 peta sebaran laporan, **#16 CD pipeline auto-deploy Railway**). Conventional commits konsisten. CODEOWNERS ada. |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **96** | **2 workflow files: `ci.yml` + `cd.yml` (separate CI & CD)**. PR #13 optimasi: timeout, concurrency, notifikasi PR gagal. PR #16 auto-deploy ke Railway pada push main. Salah satu pipeline tercanggih di kelas. |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **92** | Backend tests: `test_reports_advanced.py` + standar. Frontend Vitest: `EmptyState.test.jsx`, `FeedbackForm.test.jsx`, `FilterBar.test.jsx`, `LoadingSpinner.test.jsx`, `ReportTable.test.jsx`. `docs/testing-guide.md` (PR #14). |

**Nilai Kelompok: (95 + 96 + 92) / 3 = 94.33 → 94**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi

> W9 zero universal.

| Nama | W9 | W10 | W11 | Total |
|---|---|---|---|---|
| Aditya Laksamana P Butar Butar | 0 | 4+1 | 1 | **6** |
| Muhammad Novri Aziztra | 0 | 2+1 | 3 | **6** |
| Firni Fauziah Ramadhini | 0 | 2 | 1 | **3** |
| Salsabila Putri Zahrani | 0 | 1 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Aditya Laksamana P Butar Butar (Lead Backend)
- **Konsistensi (30%):** 2/3 → 78 · **Substansi (40%):** 6 → 78 · **Peran (20%):** Backend + tests → 86 · **Pesan (10%):** Conventional → 82

**Nilai: 23.4 + 31.2 + 17.2 + 8.2 = 80.0 → 80** · **Grade: AB**

---

#### 2. Muhammad Novri Aziztra (Lead DevOps)
- **Konsistensi (30%):** 2/3 → 78 · **Substansi (40%):** 6 commits, role CI/CD prime → 82 · **Peran (20%):** 100% match (CI optimization + CD auto-deploy) → 94 · **Pesan (10%):** → 82

**Nilai: 23.4 + 32.8 + 18.8 + 8.2 = 83.2 → 83** · **Grade: AB**

---

#### 3. Firni Fauziah Ramadhini (Lead Frontend)
- **Konsistensi (30%):** 2/3 → 75 · **Substansi (40%):** 3 (frontend tests PR #11) → 72 · **Peran (20%):** Frontend tests → 82 · **Pesan (10%):** → 80

**Nilai: 22.5 + 28.8 + 16.4 + 8.0 = 75.7 → 76** · **Grade: AB**

---

#### 4. Salsabila Putri Zahrani (Lead QA & Docs)
- **Konsistensi (30%):** 1/3 → 60 · **Substansi (40%):** 1 → 55 · **Peran (20%):** Docs (testing-guide PR #14) → 78 · **Pesan (10%):** → 78

**Nilai: 18.0 + 22.0 + 15.6 + 7.8 = 63.4 → 63** · **Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C12 (3%):** semua anggota **94**

**C13 (3%):**

| NIM | Nama | Skor | Catatan |
|---|---|:---:|---|
| 10231006 | Aditya Laksamana P Butar Butar | **80** | reguler |
| 10231038 | Firni Fauziah Ramadhini | **76** | reguler |
| 10231066 | Muhammad Novri Aziztra | **83** | reguler |
| 10231086 | Salsabila Putri Zahrani | **63** | NIM tidak di gradebook |

---

### E. Tren Lintas Fase

| Anggota | F1 | F2 | F4 |
|---|:---:|:---:|:---:|
| Aditya (Backend) | 88 | 82 | 80 |
| Firni (Frontend) | 84 | 74 | 76 |
| Novri (DevOps) | 74 | 84 | 83 |
| Salsabila (QA & Docs) | 75 | 82 | 63 |

**Nilai kelompok:** F1=87, F2=89, F4=94 → konsisten naik. Salah satu kelompok terbaik kelas B (CI+CD lengkap).
