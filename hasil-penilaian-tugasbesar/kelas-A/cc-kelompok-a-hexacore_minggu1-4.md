# Laporan Penilaian Kelompok hexacore – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexacore |
| Repo | cc-kelompok-a-hexacore |
| Kelas | A |
| Project | **LenteraPustaka** — Sistem Informasi Peminjaman Buku Perpustakaan berbasis web dengan RBAC (Admin/Member/Guest) |

**Anggota (dari README + `/team` endpoint backend/main.py:181):**

| Nama | NIM | Role |
|---|---|---|
| Maulana Malik Ibrahim | 10231051 | Lead Backend |
| Micka Mayulia Utama | 10231053 | Lead Frontend |
| Khanza Nabila Tsabita | 10231049 | Lead DevOps |
| Muhammad Aqila Ardhi | 10231057 | Lead QA & Docs |

---

### A. Penilaian Kelompok – Foundation Project (Kualitas Kode & Deliverable)

> 4 kriteria @ 25%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **92** | README komprehensif: problem statement jelas (3 pengguna: Guest/Member/Admin), masalah yang diselesaikan tertulis eksplisit, tech stack, architecture diagram, dual setup guide (Docker + Native). `/team` endpoint ada di `backend/main.py:181`. Bonus: `tentangapp.md` + `ROADMAP_LENTERA_PUSTAKA.md` + member-* docs lengkap. |
| **M2 – Backend CRUD domain-specific** | 25% | **92** | Backend FastAPI sangat lengkap, **40+ endpoint** sesuai domain perpustakaan: Categories, Genres, Books (+stats), Users, Transactions (create/approve/reject/return/lost/simulate-overdue), Fines, Upload covers/fines. Struktur layered: `models.py` (209L), `schemas.py` (341L), `crud.py` (778L), `main.py` (762L), `migrations/`, `tests/`, `pytest.ini`. RBAC business rules diterapkan. |
| **M3 – Frontend domain-specific** | 25% | **88** | React + Vite dengan struktur src/ profesional: `components/`, `pages/`, `hooks/`, `services/`, `utils/`, `test/`. Sudah ada Dockerfile + `nginx.conf` untuk serve production build. ESLint config. Halaman dan komponen sesuai domain (member/admin/book/transaction). Catatan: `refactor.py` di root frontend perlu dibersihkan. |
| **M4 – Auth + CORS + .env** | 25% | **90** | JWT lengkap (`auth.py`: create_access_token, decode, get_current_user). `SECRET_KEY`, `ALGORITHM`, `ACCESS_TOKEN_EXPIRE_MINUTES` dari env. CORS `ALLOWED_ORIGINS` dari env (`main.py:71-75`). `python-dotenv` aktif. Endpoint auth lengkap: register/login/me/change-password/profile. `.env.example` ada (dari commit `ea0f19d`). Minus: fallback `SECRET_KEY` hardcoded untuk dev — perlu di-flag di Modul 15 security audit. |

**Nilai Kelompok: (92 + 92 + 88 + 90) / 4 = 90.50**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W1–W4)

> W1 = 24 Feb–1 Mar, W2 = 2–8 Mar, W3 = 9–15 Mar, W4 = 16–22 Mar.
>
> **Catatan alias:** Aqila pakai 2 git name (`mightyqilo13` + `mightyqila13`). Khanza pakai `Khanza nabila t` + `x3naline` (email sama). Semua sudah dikonsolidasi.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Maulana Malik Ibrahim | Maulana Malik Ibrahim | 8 | 13 | 10 | 6 | **37** |
| Khanza Nabila Tsabita | Khanza nabila t / x3naline | 5 | 2 | 8 | 3 | **18** |
| Micka Mayulia Utama | micka | 6 | 4 | 5 | 3 | **18** |
| Muhammad Aqila Ardhi | mightyqilo13 / mightyqila13 | 5 | 1 | 2 | 0 | **8** |

---

### C. Penilaian Individual

> Bobot: Konsistensi 30% + Substansi 40% + Kesesuaian Peran 20% + Kualitas Pesan 10%

#### 1. Maulana Malik Ibrahim (Lead Backend)
- **Konsistensi (30%):** 4/4 minggu aktif, distribusi sangat merata → 96
- **Substansi (40%):** 37 commits — tertinggi kelompok. Mengarsiteki seluruh backend: models (Books, Users, Transactions, Fines), 40+ endpoint, RBAC, migrations, business rules (race condition pinjam bersamaan, denda, blokir member) → 94
- **Kesesuaian Peran (20%):** 100% commit di domain backend (CRUD, auth, schemas) → 95
- **Kualitas Pesan (10%):** Deskriptif dengan konteks (`Fix Role Business Rules`, `Add Auth, Genre, Book Genre`) → 86

**Nilai: (0.30×96 + 0.40×94 + 0.20×95 + 0.10×86) = 28.8 + 37.6 + 19.0 + 8.6 = 94.0 → 94**
**Grade: A**

---

#### 2. Khanza Nabila Tsabita (Lead DevOps)
- **Konsistensi (30%):** 4/4 minggu aktif → 88
- **Substansi (40%):** 18 commits; `setup.sh`, `.env.example`, `.gitignore`, env devops, setup-guide, api-documentation, ui-test-results docs. Spread DevOps + docs → 84
- **Kesesuaian Peran (20%):** Setup env, gitignore, setup.sh — sesuai DevOps. Sedikit overlap ke docs → 86
- **Kualitas Pesan (10%):** Cukup deskriptif (`env devops don`, `setup frontend environment variables`) — kadang typo (`don` bukan `done`) → 78

**Nilai: (0.30×88 + 0.40×84 + 0.20×86 + 0.10×78) = 26.4 + 33.6 + 17.2 + 7.8 = 85.0 → 85**
**Grade: AB**

---

#### 3. Micka Mayulia Utama (Lead Frontend)
- **Konsistensi (30%):** 4/4 minggu aktif → 86
- **Substansi (40%):** 18 commits; frontend awal → vol 2 → part 3 → part 4 progresif, fitur sorting, test endpoint, database part 1. Output frontend terlihat di struktur `src/` → 82
- **Kesesuaian Peran (20%):** Mayoritas commit frontend. `database part 1` sedikit out-of-role tapi acceptable di awal proyek → 84
- **Kualitas Pesan (10%):** Pesan terlalu generik (`Frontend part 4`, `frontend awal`, `test endpoin part1`) — kurang menjelaskan WHAT/WHY → 72

**Nilai: (0.30×86 + 0.40×82 + 0.20×84 + 0.10×72) = 25.8 + 32.8 + 16.8 + 7.2 = 82.6 → 83**
**Grade: AB**

---

#### 4. Muhammad Aqila Ardhi (Lead QA & Docs)
- **Konsistensi (30%):** 3/4 minggu aktif (W4 0 commit) → 70
- **Substansi (40%):** 8 commits; API documentation, test results, database schema, member info. Output docs ada (api-documentation.md, api-test-results.md, ui-test-results.md, testing-guide.md, retrospective-m1.md). Substansi cukup tapi volume kurang → 70
- **Kesesuaian Peran (20%):** 100% commit di docs/QA — sesuai peran → 85
- **Kualitas Pesan (10%):** Deskriptif dengan format conventional (`docs: add complete API documentation...`) → 82

**Nilai: (0.30×70 + 0.40×70 + 0.20×85 + 0.10×82) = 21.0 + 28.0 + 17.0 + 8.2 = 74.2 → 74**
**Grade: B**

---

### D. Ringkasan untuk Gradebook

**C02 — Tugas terstruktur kelompok (5%):** semua anggota **90**

**C03 — Partisipasi & kontribusi mingguan via Git log (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231049 | Khanza Nabila Tsabita | **85** |
| 10231051 | Maulana Malik Ibrahim | **94** |
| 10231053 | Micka Mayulia Utama | **83** |
| 10231057 | Muhammad Aqila Ardhi | **74** |

---

### E. Catatan untuk Fase Berikutnya

- ✅ Foundation project sangat kuat → siap masuk ke containerization (M5–7) dengan baseline tinggi
- ⚠️ Aqila (QA & Docs) perlu didorong velocity di Fase 2 — gap dengan anggota lain cukup besar
- ⚠️ Hardcoded fallback `SECRET_KEY` di `auth.py:23` — flag untuk Modul 15 (security audit)
- ⚠️ File `refactor.py` di root frontend dan beberapa file `image*` di root — perlu cleanup
- 💡 Pesan commit Micka terlalu generik — jika sempat, sarankan format conventional commits ke depan
