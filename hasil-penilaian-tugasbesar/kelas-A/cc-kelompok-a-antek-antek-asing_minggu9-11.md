# Laporan Penilaian Kelompok antek-antek-asing – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | antek-antek-asing |
| Repo | cc-kelompok-a-antek-antek-asing |
| Fase | M9 (Git workflow + PR) → M10 (CI dengan GitHub Actions) → M11 (Optimasi pipeline + coverage) |

---

### A. Penilaian Kelompok – CI/CD

> 3 kriteria @ ~33%. **Gap utama:** tidak ada workflow GitHub Actions di repository.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **55** | Hanya **1 PR ter-merge** dalam fase ini (`#3 chore: add CODEOWNERS for automatic reviewer assignment`). Sisanya commit direct ke main. `CODEOWNERS` di-add (positive). Branch protection tidak terlihat aktif dari pola history. |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **30** | **Tidak ada file workflow** di `.github/workflows/`. Folder `.github/` hanya berisi `CODEOWNERS`. Deliverable inti M10 (`ci.yml` dengan jobs test + build) **tidak ada**. Penalti besar. |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **58** | **Backend tests** ada: `test_auth.py`, `test_health.py`, `test_items.py` + `conftest.py`. **Frontend tests:** Vitest setup (`api.test.js`, `setup.js`). Commit "Setup Testing Backend" (`811beb2`) + "Setup Testing Frontend" (`67ffa15`) di W11. **Minus:** tidak ada CI untuk auto-run, tidak ada badge di README, tidak ada coverage threshold. |

**Nilai Kelompok: (55 + 30 + 58) / 3 = 47.67 → 48**
**Grade Kelompok: D**

> 🔴 **Action item kritis untuk Fase 5/6:** buat `ci.yml` minimal (test-backend + test-frontend + build-docker). Tes sudah ada, tinggal di-wire ke GitHub Actions. Tanpa ini, Fase 6 (M16 demo CI/CD end-to-end) tidak bisa di-deliver.

---

### B. Distribusi Kontribusi Individual (git log W9–W11)

> W9 = 20–26 Apr, W10 = 27 Apr – 3 Mei, W11 = 4–10 Mei.
> Catatan: **W10 zero commit** seluruh tim — minggu sepi.

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Muhammad Athala Romero | Muhammad Athala Romero | 3 | 0 | 1 | **4** |
| Muhammad Bagas Setiawan | Muhammaad Bagas Setiawan | 3 | 0 | 1 | **4** |
| M. Fikri Haikal Ariadma | Haikal / FikriHaikal | 1 | 0 | 1 | **2** |
| Nanda Aulia Putri | Nanda Aulia Putri | 1 | 0 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Muhammad Athala Romero (Lead Backend)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 4 commits: notification updates per role, change password profile, setup testing backend → 75
- **Kesesuaian Peran (20%):** Backend + testing → 82
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×72 + 0.40×75 + 0.20×82 + 0.10×78) = 21.6 + 30.0 + 16.4 + 7.8 = 75.8 → 76**
**Grade: AB**

---

#### 2. Muhammad Bagas Setiawan (Lead Frontend)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 4 commits: fix UI buttons, integrasi notifikasi, setup testing frontend → 75
- **Kesesuaian Peran (20%):** Frontend → 80
- **Kualitas Pesan (10%):** → 72

**Nilai: (0.30×72 + 0.40×75 + 0.20×80 + 0.10×72) = 21.6 + 30.0 + 16.0 + 7.2 = 74.8 → 75**
**Grade: B**

---

#### 3. M. Fikri Haikal Ariadma (Lead DevOps)
- **Konsistensi (30%):** 2/3 minggu aktif → 65
- **Substansi (40%):** 2 commits — termasuk `CODEOWNERS` PR. **Tidak ada CI workflow** padahal ini peran inti DevOps di fase ini → 55
- **Kesesuaian Peran (20%):** CODEOWNERS sesuai DevOps tapi missing CI delivery → 70
- **Kualitas Pesan (10%):** PR conventional → 80

**Nilai: (0.30×65 + 0.40×55 + 0.20×70 + 0.10×80) = 19.5 + 22.0 + 14.0 + 8.0 = 63.5 → 64**
**Grade: BC**

> 🔴 Sebagai Lead DevOps, gap CI workflow turun ke skor. Bila CI di-deliver di Fase 5, recovery bisa cepat.

---

#### 4. Nanda Aulia Putri (Lead QA & Docs)
- **Konsistensi (30%):** 1/3 minggu aktif → 50
- **Substansi (40%):** 1 commit (`merapikan readme`) → 50
- **Kesesuaian Peran (20%):** Docs → 60
- **Kualitas Pesan (10%):** → 70

**Nilai: (0.30×50 + 0.40×50 + 0.20×60 + 0.10×70) = 15.0 + 20.0 + 12.0 + 7.0 = 54.0 → 54**
**Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C12 — Tugas CI/CD pipeline + badge hijau (3%):** semua anggota **48**

**C13 — Kontribusi via Git commit log + PR history (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231059 | Muhammad Athala Romero | **76** |
| 10231061 | Muhammad Bagas Setiawan | **75** |
| 10231063 | Muhammad Fikri Haikal Ariadma | **64** |
| 10231067 | Nanda Aulia Putri | **54** |

---

### E. Tren Lintas Fase (antek-antek-asing)

| Anggota | F1 (M1-4) | F2 (M5-7) | F4 (M9-11) | Tren |
|---|:---:|:---:|:---:|---|
| Athala (Backend) | 81 | 77 | 76 | Stabil sedikit menurun |
| Bagas (Frontend) | 81 | 73 | 75 | Stabil |
| Haikal (DevOps) | 81 | 84 | 64 | Naik di F2, drop tajam di F4 (missing CI) |
| Nanda (QA & Docs) | 84 | 54 | 54 | Drop tajam setelah F1 |

**Nilai kelompok:** F1=87, F2=84, F4=48 → **drop signifikan di F4 karena tidak ada CI workflow**.
