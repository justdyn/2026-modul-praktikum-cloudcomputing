# Laporan Penilaian Kelompok hexacore – Kelas A
## Fase 4: Minggu Kuliah 9–11 (20 Apr – 10 Mei 2026) — CI/CD Pipeline

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexacore |
| Repo | cc-kelompok-a-hexacore |
| Fase | M9 (Git workflow + PR) → M10 (CI dengan GitHub Actions) → M11 (Optimasi pipeline + coverage) |

---

### A. Penilaian Kelompok – CI/CD (Kualitas Pipeline)

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M9 – Git workflow + PR history** | 33% | **94** | **18 PR ter-merge** dalam fase ini (visible dari `Merge pull request #X` dan `(#XX)` di squash commit). Branch protection di-honor (Maulana cross-merge PR Backend, Khanza PR DevOps). `CODEOWNERS` di `.github/CODEOWNERS` untuk auto-assign reviewer (commit `2065040`). `git-workflow-guide.md` di `docs/` sebagai panduan tim. Conventional commits sudah dipakai (feat:, test:, docs:, chore:). |
| **M10 – CI pipeline (GitHub Actions YAML)** | 33% | **96** | `.github/workflows/ci.yml` sangat solid: **3 jobs** (test-backend pytest, test-frontend Vitest, build-docker). Concurrency cancel-in-progress (anti-resource-waste). pip cache + npm cache. Timeout 10 menit per job. `needs: [test-backend, test-frontend]` untuk gate Docker build (tests harus hijau dulu). Setup-python@v5, setup-node@v4 versi terbaru. Coverage gate `--cov-fail-under=50` — punya quality gate eksplisit. |
| **M11 – Test coverage + badge + dokumentasi** | 34% | **92** | **Backend tests:** 9 file di `backend/tests/` (test_auth, test_books, test_categories, test_fines, test_genres, test_health, test_transactions, test_uploads, test_users) + `conftest.py`. **Frontend tests:** Vitest setup (`api.test.js`, `setup.js`). CI badge muncul di README (`![CI Pipeline](.../ci.yml/badge.svg)`). Dokumentasi pendukung: `docs/testing-guide.md`, SOP "panduan testing dan pembacaan log CI" (PR #18). Minus: coverage threshold 50% relatif rendah — di Modul 15 bisa dinaikkan. |

**Nilai Kelompok: (94 + 96 + 92) / 3 = 94.00**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W9–W11)

> W9 = 20–26 Apr, W10 = 27 Apr – 3 Mei, W11 = 4–10 Mei.
>
> **Alias diperluas:** Khanza pakai `x3naline` di fase ini (semua commit DevOps); Aqila pakai mix `mightyqilo13` + `mightyqila13`; Micka pakai `micka` + `mickamayulia`. Semua dikonsolidasi.

| Nama | Git Name(s) | W9 | W10 | W11 | Total |
|---|---|---|---|---|---|
| Muhammad Aqila Ardhi | mightyqilo13 / mightyqila13 | 2 | 0 | 5 | **7** |
| Maulana Malik Ibrahim | Maulana Malik Ibrahim | 2 | 0 | 3 | **5** |
| Micka Mayulia Utama | micka / mickamayulia | 1 | 1 | 3 | **5** |
| Khanza Nabila Tsabita | x3naline | 0 | 3 | 1 | **4** |

> 📌 Aqila naik ke posisi 1 — switch role dominan. Distribusi sekarang lebih merata (range 4–7 vs sebelumnya 3–13). Sehat untuk fase CI/CD yang membutuhkan kontribusi paralel dari semua role.

---

### C. Penilaian Individual

#### 1. Khanza Nabila Tsabita (Lead DevOps / Lead CI/CD)
- **Konsistensi (30%):** 2/3 minggu aktif (W9 kosong) → 75
- **Substansi (40%):** 4 commits tapi **paling crucial**: `CODEOWNERS` setup (#4), `docker-compose.prod.yml` production profile (#5), `Makefile` automation (#6), **optimized CI pipeline + badge** (#16). Semua adalah inti penilaian M9–11 → 92
- **Kesesuaian Peran (20%):** 100% commit CI/CD + DevOps — sangat sesuai role → 98
- **Kualitas Pesan (10%):** Conventional commits dengan deskripsi panjang (`feat: add optimized CI pipeline and update README by adding status badge`) → 90

**Nilai: (0.30×75 + 0.40×92 + 0.20×98 + 0.10×90) = 22.5 + 36.8 + 19.6 + 9.0 = 87.9 → 88**
**Grade: A**

> 💡 Volume rendah tapi *impact per commit* tinggi. Setiap commit Khanza adalah deliverable utama M9–11.

---

#### 2. Muhammad Aqila Ardhi (Lead QA & Docs)
- **Konsistensi (30%):** 2/3 minggu aktif (W10 kosong) → 80
- **Substansi (40%):** 7 commits: layout docs UTS, retrospective M1 (#10), git workflow guide (#11), merge README docs update (#12), README CI badge (#17), SOP testing & log CI (#18). Output dokumentasi sangat lengkap dan langsung ter-merge sebagai PR → 88
- **Kesesuaian Peran (20%):** 100% commit docs → 95
- **Kualitas Pesan (10%):** Conventional commits Bahasa Indonesia konsisten (`docs: menambahkan lencana (badge) status CI Pipeline di README`) → 92

**Nilai: (0.30×80 + 0.40×88 + 0.20×95 + 0.10×92) = 24.0 + 35.2 + 19.0 + 9.2 = 87.4 → 87**
**Grade: A**

> 📈 Konsisten naik: Fase 1 = 74 (B) → Fase 2 = 83 (AB) → Fase 4 = 87 (A). Progress paling impresif di tim.

---

#### 3. Maulana Malik Ibrahim (Lead Backend)
- **Konsistensi (30%):** 2/3 minggu aktif (W10 kosong) → 80
- **Substansi (40%):** 5 commits: validasi format ISBN, bantu frontend fix ISBN (cross-role help), database health check endpoint (#9, *crucial untuk CI test*), merge feature/item-categories (#8), backend pytest coverage tests (#14, *crucial M11*). Substansi langsung mendukung pipeline pass → 88
- **Kesesuaian Peran (20%):** 100% commit backend + tests → 92
- **Kualitas Pesan (10%):** Conventional commits dengan deskripsi (`feat: add database health check endpoint`, `test: add backend pytest coverage tests`) → 88

**Nilai: (0.30×80 + 0.40×88 + 0.20×92 + 0.10×88) = 24.0 + 35.2 + 18.4 + 8.8 = 86.4 → 86**
**Grade: A**

---

#### 4. Micka Mayulia Utama (Lead Frontend)
- **Konsistensi (30%):** 3/3 minggu aktif → 88
- **Substansi (40%):** 5 commits: book cover upload (W9), refactor App.jsx + docker + bug fix (W10), about page team members (#7), Feature/dark mode (#13), Vitest setup + frontend unit tests (#15, *crucial M11*). Vitest setup adalah deliverable utama frontend testing → 84
- **Kesesuaian Peran (20%):** Sangat sesuai (frontend feature + frontend tests) → 90
- **Kualitas Pesan (10%):** Conventional commits konsisten (`feat: add book cover upload support`, `test: setup Vitest and add frontend unit tests`) — improvement signifikan dari Fase 1 → 86

**Nilai: (0.30×88 + 0.40×84 + 0.20×90 + 0.10×86) = 26.4 + 33.6 + 18.0 + 8.6 = 86.6 → 87**
**Grade: A**

> 📈 Naik dari AB (83) di Fase 1 → AB (76) di Fase 2 → A (87) di Fase 4. Kualitas commit naik tajam.

---

### D. Ringkasan untuk Gradebook

**C12 — Tugas CI/CD pipeline + badge hijau (3%):** semua anggota **94**

**C13 — Kontribusi via Git commit log + PR history (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231049 | Khanza Nabila Tsabita | **88** |
| 10231051 | Maulana Malik Ibrahim | **86** |
| 10231053 | Micka Mayulia Utama | **87** |
| 10231057 | Muhammad Aqila Ardhi | **87** |

---

### E. Tren Lintas Fase (Hexacore)

| Anggota | F1 (M1-4) | F2 (M5-7) | F4 (M9-11) | Tren |
|---|:---:|:---:|:---:|:---:|
| Maulana Malik Ibrahim | 94 | 87 | 86 | Konsisten tinggi, sedikit turun |
| Khanza Nabila Tsabita | 85 | 91 | 88 | Konsisten naik |
| Micka Mayulia Utama | 83 | 76 | 87 | Recover kuat di F4 |
| Muhammad Aqila Ardhi | 74 | 83 | 87 | **Naik tajam tiap fase** |

**Nilai kelompok:** F1=90.5, F2=93.3, F4=94.0 → konsisten naik, project mature.

---

### F. Catatan untuk Fase Berikutnya (M12–14: Microservices & M15–16: Final)

- ✅ Foundation CI/CD profesional → siap decompose ke microservices tanpa breaking pipeline
- 💡 Untuk M12–14: pertimbangkan split workflow per-service jika service di-decompose
- ⚠️ Coverage gate masih 50% — flag untuk M15 final polish (rekomendasi naikkan ke 70%)
- ⚠️ Hardcoded `POSTGRES_PASSWORD: postgres` dari Fase 2 belum di-fix — pasti muncul di M15 security audit
- 💡 Semua anggota sekarang stabil di range 86–88 — distribusi paling sehat di kelas (asumsi)
