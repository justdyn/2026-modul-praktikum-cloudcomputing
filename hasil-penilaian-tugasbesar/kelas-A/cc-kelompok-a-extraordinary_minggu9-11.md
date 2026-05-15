# Laporan Penilaian Kelompok extraordinary – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### A. Penilaian Kelompok – CI/CD

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **60** | `.github/CODEOWNERS` ada. PR usage di F4 minim — tidak ada PR ter-merge yang terlihat di window F4. Mayoritas commit direct ke main. |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **30** | **Tidak ada file workflow** di `.github/workflows/`. Folder `.github/` hanya berisi `CODEOWNERS`. Deliverable inti M10 tidak ada. |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **72** | Tests bagus: `test_auth_service.py`, `test_claim_service.py`, `test_item_service.py`, `test_search_sanitization.py`, `test_user_schema.py` (5 file, termasuk security test). Tidak ada CI untuk auto-run, tidak ada badge. |

**Nilai Kelompok: (60 + 30 + 72) / 3 = 54.00 → 54**
**Grade Kelompok: BC**

---

### B. Distribusi Kontribusi Individual

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Rani Ayu Dewi | raniayudewi | 8 | 0 | 4 | **12** |
| Pangeran Borneo Silaen | PangeranSilaen / Pangeran Borneo Silaen | 2 | 0 | 6 | **8** |
| Raisha Alika Irwandira | disnejy | 1 | 0 | 0 | **1** |
| Nicholas Christian S. Manurung | — | 0 | 0 | 0 | **0** |

---

### C. Penilaian Individual

#### 1. Pangeran Borneo Silaen (Lead DevOps)
- **Konsistensi (30%):** 2/3 → 72 · **Substansi (40%):** 8 commits, tapi tidak ada CI workflow padahal Lead DevOps → 60 · **Peran (20%):** DevOps tanpa CI deliverable → 65 · **Pesan (10%):** → 78

**Nilai: 21.6 + 24.0 + 13.0 + 7.8 = 66.4 → 66** · **Grade: B**

---

#### 2. Rani Ayu Dewi (Lead QA & Docs)
- **Konsistensi (30%):** 2/3 → 80 · **Substansi (40%):** 12 commits, tertinggi tim → 82 · **Peran (20%):** Docs → 84 · **Pesan (10%):** → 78

**Nilai: 24.0 + 32.8 + 16.8 + 7.8 = 81.4 → 81** · **Grade: AB**

---

#### 3. Raisha Alika Irwandira (Lead Backend)
- **Konsistensi (30%):** 1/3 → 50 · **Substansi (40%):** 1 commit → 50 · **Peran (20%):** Backend → 65 · **Pesan (10%):** → 70

**Nilai: 15.0 + 20.0 + 13.0 + 7.0 = 55.0 → 55** · **Grade: BC**

---

#### 4. Nicholas Christian Samuel Manurung (Lead Frontend)
- **Konsistensi (30%):** 0/3 → 40 · **Substansi (40%):** 0 commits → 40 · **Peran (20%):** → 50 · **Pesan (10%):** → 50

**Nilai: 12.0 + 16.0 + 10.0 + 5.0 = 43.0 → 43** · **Grade: D**

---

### D. Ringkasan untuk Gradebook

**C12 (3%):** semua anggota **54**

**C13 (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231069 | Nicholas Christian Samuel Manurung | **43** |
| 10231073 | Pangeran Borneo Silaen | **66** |
| 10231077 | Raisha Alika Irwandira | **55** |
| 10231079 | Rani Ayu Dewi | **81** |

---

### E. Tren Lintas Fase (extraordinary)

| Anggota | F1 | F2 | F4 |
|---|:---:|:---:|:---:|
| Nicholas (Frontend) | 70 | 79 | 43 |
| Pangeran (DevOps) | 85 | 88 | 66 |
| Raisha (Backend) | 75 | 79 | 55 |
| Rani (QA & Docs) | 81 | 70 | 81 |

**Nilai kelompok:** F1=88, F2=89, F4=54 → drop tajam di F4 karena tidak ada CI workflow (mirip antek-antek-asing).
