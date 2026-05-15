# Laporan Penilaian Kelompok nexa – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nexa |
| Repo | cc-kelompok-a-nexa |
| Project | **Studyfy** — Learning Management System (LMS) berbasis cloud dengan 3 role (admin, pengajar, murid): materi multimedia, dashboard pengajar, penilaian, RBAC pengguna |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Dhiya Afifah | 10231031 | Lead Frontend |
| Dzaky Rasyiq Zuhair | 10231035 | Lead Backend |
| Gabriel Karmen Sanggalangi | 10231039 | Lead QA & Docs |
| Ika Agustin Wulandari | 10231041 | Lead DevOps |

---

### A. Penilaian Kelompok – Foundation Project

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **88** | README LMS detailed dengan 3 role, urgensi pendidikan digital. **`/team` endpoint EXISTS** (`backend/main.py:601`). Member-specific docs: `docs-Gabriel.md`, `docs-Wulan.md`. Plus `FEATURE_USER_MANAGEMENT.md`, `IMPLEMENTATION_CHECKLIST.md`, `QUICK_START_TESTING.md`. |
| **M2 – Backend CRUD domain-specific** | 25% | **86** | 32 routes di `main.py`. `full_migration.sql` + `migration.sql` menunjukkan schema versioning aktif. Layered: models/schemas/crud/auth/database. `test_connection.py` di root backend (utility). |
| **M3 – Frontend domain-specific** | 25% | **84** | Standard React+Vite untuk LMS. |
| **M4 – Auth + CORS + .env** | 25% | **86** | JWT, CORS dari env (`ALLOWED_ORIGINS=http://localhost:5173,http://localhost`), `PASSWORD_RESET_TOKEN_EXPIRE_MINUTES` (feature lanjut). Minus: fallback hardcoded SECRET_KEY (`auth.py:19`). |

**Nilai Kelompok: (88 + 86 + 84 + 86) / 4 = 86.00**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual

> **Catatan alias:** Ika = `Ika Agustin Wulandari` + `10231041-cloud`. Dzaky = `dzaky rasyiq zuhair` + `Dzaky rasyiq zuhair`. Gabriel = `Gabriel Karmen` + `Gabriel Karmen Sanggalangi`. Dhiya = `Dhiya Afifah` + `Dhiya`.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Gabriel Karmen Sanggalangi | Gabriel Karmen | 2 | 6 | 1 | 0 | **9** |
| Dzaky Rasyiq Zuhair | dzaky rasyiq zuhair | 4 | 1 | 0 | 3 | **8** |
| Dhiya Afifah | Dhiya Afifah | 1 | 5 | 1 | 0 | **7** |
| Ika Agustin Wulandari | Ika Agustin Wulandari | 0 | 5 | 0 | 0 | **5** |

---

### C. Penilaian Individual

#### 1. Gabriel Karmen Sanggalangi (Lead QA & Docs)
- **Konsistensi (30%):** 3/4 → 82 · **Substansi (40%):** 9 commits → 80 · **Peran (20%):** Docs (docs-Gabriel.md sesuai role) → 86 · **Pesan (10%):** → 78

**Nilai: 24.6 + 32.0 + 17.2 + 7.8 = 81.6 → 82** · **Grade: AB**

---

#### 2. Dzaky Rasyiq Zuhair (Lead Backend)
- **Konsistensi (30%):** 3/4 → 80 · **Substansi (40%):** 8 commits backend → 78 · **Peran (20%):** Backend → 86 · **Pesan (10%):** → 75

**Nilai: 24.0 + 31.2 + 17.2 + 7.5 = 79.9 → 80** · **Grade: AB**

---

#### 3. Dhiya Afifah (Lead Frontend)
- **Konsistensi (30%):** 3/4 → 80 · **Substansi (40%):** 7 commits frontend → 76 · **Peran (20%):** Frontend → 84 · **Pesan (10%):** → 75

**Nilai: 24.0 + 30.4 + 16.8 + 7.5 = 78.7 → 79** · **Grade: AB**

---

#### 4. Ika Agustin Wulandari (Lead DevOps)
- **Konsistensi (30%):** 1/4 (W2 only) → 55 · **Substansi (40%):** 5 commits → 65 · **Peran (20%):** DevOps belum F1 prime → 70 · **Pesan (10%):** → 72

**Nilai: 16.5 + 26.0 + 14.0 + 7.2 = 63.7 → 64** · **Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C02 (5%):** semua anggota **86**

**C03 (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231031 | Dhiya Afifah | **79** |
| 10231035 | Dzaky Rasyiq Zuhair | **80** |
| 10231039 | Gabriel Karmen Sanggalangi | **82** |
| 10231041 | Ika Agustin Wulandari | **64** |
