# Laporan Penilaian Kelompok nexa – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### A. Penilaian Kelompok – CI/CD

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **65** | `CODEOWNERS` ada. **Hanya 1 PR ter-merge** dalam window F4 (PR #2 CODEOWNERS). Mayoritas commit direct ke main meski infra siap. |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **82** | **2 workflow files**: `ci-testing.yml` + `main.yml` (split testing dari main pipeline — pendekatan yang valid). |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **70** | **Tidak ada folder `backend/tests/`** — hanya `test_connection.py` di root backend (utility script, bukan test framework). Dokumentasi `QUICK_START_TESTING.md` ada tapi tidak ada test file terstruktur. |

**Nilai Kelompok: (65 + 82 + 70) / 3 = 72.33 → 72**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Gabriel Karmen Sanggalangi | Gabriel Karmen | 2 | 3 | 1 | **6** |
| Dhiya Afifah | Dhiya | 5 | 1 | 0 | **6** |
| Dzaky Rasyiq Zuhair | dzaky / Dzaky | 3 | 3 | 0 | **6** |
| Ika Agustin Wulandari | Ika + 10231041-cloud | 1 | 0 | 3 | **4** |

---

### C. Penilaian Individual

#### 1. Gabriel Karmen Sanggalangi (Lead QA & Docs)
- **Konsistensi (30%):** 3/3 → 88 · **Substansi (40%):** 6 commits → 75 · **Peran (20%):** Docs → 84 · **Pesan (10%):** → 78

**Nilai: 26.4 + 30.0 + 16.8 + 7.8 = 81.0 → 81** · **Grade: AB**

---

#### 2. Dhiya Afifah (Lead Frontend)
- **Konsistensi (30%):** 2/3 → 75 · **Substansi (40%):** 6 commits → 75 · **Peran (20%):** Frontend → 80 · **Pesan (10%):** → 75

**Nilai: 22.5 + 30.0 + 16.0 + 7.5 = 76.0 → 76** · **Grade: AB**

---

#### 3. Dzaky Rasyiq Zuhair (Lead Backend)
- **Konsistensi (30%):** 2/3 → 75 · **Substansi (40%):** 6 commits → 75 · **Peran (20%):** Backend → 80 · **Pesan (10%):** → 75

**Nilai: 22.5 + 30.0 + 16.0 + 7.5 = 76.0 → 76** · **Grade: AB**

---

#### 4. Ika Agustin Wulandari (Lead DevOps)
- **Konsistensi (30%):** 2/3 → 72 · **Substansi (40%):** 4 commits → 68 · **Peran (20%):** DevOps/CI prime → 82 · **Pesan (10%):** → 75

**Nilai: 21.6 + 27.2 + 16.4 + 7.5 = 72.7 → 73** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C12 (3%):** semua anggota **72**

**C13 (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231031 | Dhiya Afifah | **76** |
| 10231035 | Dzaky Rasyiq Zuhair | **76** |
| 10231039 | Gabriel Karmen Sanggalangi | **81** |
| 10231041 | Ika Agustin Wulandari | **73** |

---

### E. Tren Lintas Fase (nexa)

| Anggota | F1 | F2 | F4 |
|---|:---:|:---:|:---:|
| Dhiya (Frontend) | 79 | 43 | 76 |
| Dzaky (Backend) | 80 | 43 | 76 |
| Gabriel (QA & Docs) | 82 | 78 | 81 |
| Ika (DevOps) | 64 | 78 | 73 |

**Nilai kelompok:** F1=86, F2=84, F4=72 → menurun di F4 karena tests tidak terstruktur + PR usage rendah.
