# Laporan Penilaian Kelompok miracle – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### A. Penilaian Kelompok – CI/CD

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **95** | **10+ PR ter-merge dalam F4** (PR #14 sampai #24+ termasuk: `add CI pipeline`, `optimize workflow with timeout/concurrency/failure notification` #16, `Feature/lint ci` #22-#24). Conventional commits konsisten. `CODEOWNERS` + `pull_request_template.md` + `copilot-instructions.md` di `.github/`. |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **92** | `.github/workflows/ci.yml` ada. Berdasarkan commit history: timeout, concurrency, failure notification, ruff linting (PR #22-#24). |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **90** | **7 backend tests** termasuk domain-spesifik (`test_auth`, `test_health`, `test_items`, `test_pendonor`, `test_riwayat_donor`) + `conftest.py`. Testing guide PR #18. Edge cases di README PR #17. |

**Nilai Kelompok: (95 + 92 + 90) / 3 = 92.33 → 92**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual

> Burst W11 seluruh tim — sprint final F4.

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Debora Intania Subekti | intniaaa20 + Debora | 0 | 3 | 12 | **15** |
| Betran | BETRAN + Betran + chelolv15? no = piz4rroo | 10 | 0 | 4 | **14** |
| Yosan Pratiwi | Yosan Pratiwi | 0 | 3 | 8 | **11** |
| Chelsy Olivia | Chelsy Olivia + chelolv15 | 0 | 2 | 8 | **10** |
| Avhilla Catton Andalucia | Avhilla + Avhilla Catton Andalucia | 2 | 1 | 6 | **9** |

---

### C. Penilaian Individual

#### 1. Chelsy Olivia (Lead CI/CD & Deploy)
- **Konsistensi (30%):** 2/3 → 80 · **Substansi (40%):** 10 commits — **role CI/CD prime time**, kontribusi CI feature work (`Feature/lint ci`, `Feature/add ci pipeline`) → 90 · **Peran (20%):** 100% match → 95 · **Pesan (10%):** Conventional → 88

**Nilai: 24.0 + 36.0 + 19.0 + 8.8 = 87.8 → 88** · **Grade: A**

---

#### 2. Debora Intania Subekti (Lead Backend)
- **Konsistensi (30%):** 2/3 → 80 · **Substansi (40%):** 15 commits, tertinggi tim → 88 · **Peran (20%):** Backend tests → 88 · **Pesan (10%):** → 80

**Nilai: 24.0 + 35.2 + 17.6 + 8.0 = 84.8 → 85** · **Grade: AB**

---

#### 3. Betran (Lead QA & Docs)
- **Konsistensi (30%):** 2/3 → 78 · **Substansi (40%):** 14 commits — testing guide, edge cases docs → 86 · **Peran (20%):** Docs/QA → 88 · **Pesan (10%):** → 80

**Nilai: 23.4 + 34.4 + 17.6 + 8.0 = 83.4 → 83** · **Grade: AB**

---

#### 4. Yosan Pratiwi (Lead Frontend)
- **Konsistensi (30%):** 2/3 → 75 · **Substansi (40%):** 11 commits → 82 · **Peran (20%):** Frontend → 84 · **Pesan (10%):** → 78

**Nilai: 22.5 + 32.8 + 16.8 + 7.8 = 79.9 → 80** · **Grade: AB**

---

#### 5. Avhilla Catton Andalucia (Lead Container)
- **Konsistensi (30%):** 3/3 → 88 · **Substansi (40%):** 9 commits → 78 · **Peran (20%):** Container/CI build → 82 · **Pesan (10%):** → 78

**Nilai: 26.4 + 31.2 + 16.4 + 7.8 = 81.8 → 82** · **Grade: AB**

---

### D. Ringkasan untuk Gradebook

**C12 (3%):** semua anggota **92**

**C13 (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231021 | Avhilla Catton Andalucia | **82** |
| 10231023 | Betran | **83** |
| 10231025 | Chelsy Olivia | **88** |
| 10231029 | Debora Intania Subekti | **85** |
| 10231091 | Yosan Pratiwi | **80** |

---

### E. Tren Lintas Fase (miracle)

| Anggota | F1 | F2 | F4 |
|---|:---:|:---:|:---:|
| Avhilla (Container) | 83 | **91** | 82 |
| Betran (QA & Docs) | 82 | 55 | 83 |
| Chelsy (CI/CD) | 80 | 60 | **88** |
| Debora (Backend) | 90 | 78 | 85 |
| Yosan (Frontend) | 87 | 72 | 80 |

**Nilai kelompok:** F1=86, F2=90, F4=92 → konsisten naik. Role-fit terlihat: Avhilla F2 prime, Chelsy F4 prime.
